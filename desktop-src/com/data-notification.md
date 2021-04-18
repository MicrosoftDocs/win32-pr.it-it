---
title: Notifica dati
description: Gli oggetti che utilizzano dati provenienti da un'origine esterna talvolta devono essere informati quando vengono modificati i dati di tale origine.
ms.assetid: 286a1ecf-5255-4443-a17d-5ffa55ed0be1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49df9e6bb7d9b15192473b18114fe7fcd69ecedf
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300513"
---
# <a name="data-notification"></a>Notifica dati

Gli oggetti che utilizzano dati provenienti da un'origine esterna talvolta devono essere informati quando vengono modificati i dati di tale origine. Ad esempio, un visualizzatore di nastri delle scorte che si basa sui dati in un foglio di calcolo deve ricevere una notifica quando i dati vengono modificati in modo che sia possibile aggiornarne la visualizzazione. Analogamente, un documento composto necessita di informazioni sulle modifiche ai dati negli oggetti incorporati, in modo che possa aggiornare le cache dei dati. In casi come questo, in cui è auspicabile l'aggiornamento dinamico dei dati, le origini dei dati richiedono un meccanismo di notifica ai consumer di modifiche apportate senza obbligare gli utenti a eliminare tutto per aggiornare i dati. Idealmente, dopo aver ricevuto una notifica che si è verificata una modifica nell'origine dati, un oggetto consumer può richiedere una copia aggiornata a piacimento.

Il meccanismo COM per la gestione delle notifiche asincrone di questo tipo è un oggetto denominato sink di notifica, che è semplicemente un oggetto COM che implementa un'interfaccia denominata [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink). I consumer di dati implementano **IAdviseSink**. Si registrano per ricevere le notifiche inviando un puntatore all'oggetto dati di interesse.

Le interfacce [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink) espone i metodi seguenti per la ricezione di notifiche asincrone:



| Metodo                                                      | Notifica al sink advise che                                            |
|-------------------------------------------------------------|--------------------------------------------------------------------------|
| [**OnDataChange**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-ondatachange)<br/> | I dati dell'oggetto chiamante sono stati modificati.<br/>                        |
| [**OnViewChange**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onviewchange)<br/> | Le istruzioni per il disegno dell'oggetto chiamante sono state modificate.<br/> |
| [**OnRename**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onrename)<br/>         | Il moniker dell'oggetto chiamante è stato modificato.<br/>                     |
| [**OnSave**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onsave)<br/>             | L'oggetto chiamante è stato salvato nell'archivio permanente.<br/>      |
| [**OnClose**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onclose)<br/>           | L'oggetto chiamante è stato chiuso.<br/>                           |



 

Come indicato nella tabella, l'interfaccia [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink) espone metodi per notificare al sink advise gli eventi diversi dalle modifiche nei dati dell'oggetto chiamante. L'oggetto chiamante può anche inviare una notifica al sink quando il modo in cui disegna le modifiche o viene rinominato, salvato o chiuso. Queste altre notifiche vengono utilizzate principalmente o interamente nel contesto dei documenti composti, anche se il meccanismo di notifica è identico. Per ulteriori informazioni sulle notifiche dei documenti composti, vedere "documenti composti".

Per sfruttare i vantaggi del sink di notifica, un'origine dati deve implementare [**IDataObject::D advise**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-dadvise), [**IDataObject::D Unadvise**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-dunadvise)e [**IDataObject:: EnumDAdvise**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumdadvise). Un consumer di dati chiama il Mothod **DAdvise** per notificare a un oggetto dati che desidera ricevere una notifica quando i dati dell'oggetto cambiano. L'oggetto consumer chiama il metodo **DUnadvise** per eliminare questa connessione. Qualsiasi parte interessata può chiamare il metodo **EnumDAdvise** per apprendere il numero di oggetti che dispongono di una connessione consultiva a un oggetto dati.

Quando i dati vengono modificati nell'origine, l'oggetto dati chiama [**IAdviseSink:: OnDataChange**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-ondatachange) su tutti i consumer di dati che hanno effettuato la registrazione per la ricezione delle notifiche. Per tenere traccia delle connessioni consultive e gestire l'invio di notifiche, le origini dati si basano su un oggetto denominato *titolare dell'avviso dati*. È possibile creare il proprio titolare di consulenza dati implementando l'interfaccia [**IDataAdviseHolder**](/windows/desktop/api/ObjIdl/nn-objidl-idataadviseholder) . In alternativa, è possibile consentire a COM di eseguire questa operazione chiamando la funzione di supporto [**CreateDataAdviseHolder**](/windows/win32/api/ole2/nf-ole2-createdataadviseholder).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Trasferimento dati](data-transfer.md)
</dt> </dl>

 

