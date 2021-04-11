---
title: Oggetto di esclusione reciproca
description: Oggetto di esclusione reciproca
ms.assetid: dd1f7865-e409-4bf9-9fa0-769a29eaed60
keywords:
- Windows Media Format SDK, oggetti di esclusione reciproca
- ASF (Advanced Systems Format), oggetti di esclusione reciproca
- ASF (Advanced Systems Format), oggetti di esclusione reciproca
- oggetti, oggetti di esclusione reciproca
- esclusione reciproca, oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8522b66f82bd88479b8c7b1d0d0b45bd038fdab3
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "104117442"
---
# <a name="mutual-exclusion-object"></a>Oggetto di esclusione reciproca

Un oggetto di esclusione reciproca viene usato per specificare un numero di flussi, di cui è possibile recapitare solo uno alla volta. Questo può essere usato in diversi modi, ad esempio fornendo un flusso audio in diversi linguaggi come colonna sonora per un flusso video.

L'esclusione reciproca è una parte facoltativa di un profilo. È possibile creare oggetti di esclusione reciproca per le informazioni di esclusione reciproca esistenti in un profilo o crearli vuoti, pronti per la ricezione di nuovi dati. Gli oggetti di esclusione reciproca non possono esistere indipendentemente da un oggetto profilo. Per salvare il contenuto di un oggetto di esclusione reciproca, è necessario chiamare [**IWMProfile:: AddMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion).

Per creare un oggetto di esclusione reciproca, usare uno dei metodi seguenti.



| Metodo                                                                              | Descrizione                                                                                                                                                 |
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMProfile::CreateNewMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion) | Crea un oggetto di esclusione reciproca senza dati.                                                                                                         |
| [**IWMProfile::GetMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getmutualexclusion)             | Crea un oggetto di esclusione reciproca popolato con i dati di un profilo. Usa l'indice di esclusione reciproca per identificare le informazioni desiderate di esclusione reciproca. |



 

In entrambi i metodi della tabella precedente è stato impostato un puntatore a un'interfaccia **IWMMutualExclusion** . L'interfaccia **IWMStreamList** viene ereditata da **IWMMutualExclusion** e non è mai necessario accedervi direttamente. L'altra interfaccia dell'oggetto di esclusione reciproca può essere ottenuta chiamando il metodo **QueryInterface** .

Le interfacce seguenti sono supportate da ogni oggetto di esclusione reciproca.



| Interfaccia                                          | Descrizione                                                                                                                                            |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMMutualExclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)   | Imposta e recupera il tipo di esclusione reciproca da utilizzare.                                                                                            |
| [**IWMMutualExclusion2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2) | Organizza i flussi nei record, che possono essere usati per creare scenari di esclusione reciproca complessi. Eredita tutti i metodi di **IWMMutualExclusion**. |
| [**IWMStreamList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)             | Gestisce l'elenco di flussi che si escludono a vicenda.                                                                                                        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Esclusione reciproca**](mutual-exclusion.md)
</dt> <dt>

[**Oggetti**](objects.md)
</dt> <dt>

[**Oggetto Gestione profili**](profile-manager-object.md)
</dt> </dl>

 

 




