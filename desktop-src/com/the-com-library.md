---
title: Libreria COM
description: Libreria COM
ms.assetid: 51d4db4a-ad88-4627-8140-2f7906945752
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a285a89ca659907c37f92b7d00f3e3e04d0acf51
ms.sourcegitcommit: 307b14e9847ced354a52a1ac12d7f659722d99bb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/06/2020
ms.locfileid: "103956249"
---
# <a name="the-com-library"></a>Libreria COM

Qualsiasi processo che utilizza COM deve inizializzare e annullare l'inizializzazione della libreria COM. Oltre a essere una specifica, COM implementa anche alcuni servizi importanti in questa libreria. Fornito come set di dll ed exe (principalmente Ole32.dll e Rpcss.exe) in Microsoft Windows, la libreria COM include quanto segue:

-   Un numero ridotto di funzioni fondamentali che semplificano la creazione di applicazioni COM, sia client che server. Per i client, COM fornisce funzioni di base per la creazione di oggetti. Per i server, COM fornisce i mezzi per esporre i relativi oggetti.

-   Implementazione-servizi del localizzatore tramite cui COM determina, da un identificatore di classe univoco (CLSID), il server che implementa la classe e la posizione in cui si trova il server. Questo servizio include il supporto per un livello di riferimento indiretto, in genere un registro di sistema, tra l'identità di una classe di oggetti e la creazione di pacchetti dell'implementazione in modo che i client siano indipendenti dalla creazione di pacchetti, che può cambiare in futuro.

-   Chiamate di procedure remote trasparenti quando un oggetto è in esecuzione in un server locale o remoto.

-   Meccanismo standard per consentire a un'applicazione di controllare la modalità di allocazione della memoria all'interno del processo, in particolare la memoria che deve essere passata tra oggetti cooperanti in modo che possa essere liberata correttamente.

Per usare i servizi COM di base, tutti i thread COM di esecuzione nei client e nei server out-of-process devono chiamare la funzione [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) o [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) prima di chiamare qualsiasi altra funzione com eccetto le chiamate di allocazione di memoria. **CoInitializeEx** sostituisce l'altra funzione, aggiungendo un parametro che consente di specificare il modello di threading del thread, ovvero con threading Apartment o a thread libero. Una chiamata a **CoInitialize** imposta semplicemente il modello di threading su Apartment-Threaded.

Le applicazioni per documenti compositi OLE chiamano la funzione [**OleInitialize**](/windows/desktop/api/Ole2/nf-ole2-oleinitialize) , che chiama [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) ed esegue anche alcune inizializzazioni necessarie per i documenti composti. Di conseguenza, i thread che chiamano **OleInitialize** non possono essere a thread libero. Per informazioni sul threading in client e server, vedere [processi, thread e Apartment](processes--threads--and-apartments.md).

I server in-process non chiamano le funzioni di inizializzazione perché vengono caricati in un processo che lo ha già fatto. Di conseguenza, i server in-process devono impostare il modello di threading nel registro di sistema nella chiave [InprocServer32](inprocserver32.md) . Per informazioni dettagliate sui problemi di threading nei server in-process, vedere [problemi di threading del server in-process](in-process-server-threading-issues.md).

È inoltre importante annullare l'inizializzazione della libreria. Per ogni chiamata a [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) o [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex), è necessario che sia presente una chiamata corrispondente a [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize). Per ogni chiamata a [**OleInitialize**](/windows/desktop/api/Ole2/nf-ole2-oleinitialize), è necessario che sia presente una chiamata corrispondente a [**OleUninitialize**](/windows/desktop/api/Ole2/nf-ole2-oleuninitialize).

I server in-process possono presupporre che il processo in cui sono stati caricati abbia già eseguito questi passaggi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Component Object Model (COM)](the-component-object-model.md)
</dt> </dl>

 

 




