---
description: API del codificatore
ms.assetid: 3d19152f-17a3-4576-a2a2-5b827d9ca8d1
title: API del codificatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 386b964f44dc4dc69896ead34bbe0d0177b198a1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401285"
---
# <a name="encoder-api"></a>API del codificatore

L'API del codificatore fornisce un'interfaccia uniforme per la configurazione dei codificatori software e hardware. Le applicazioni possono usare l'API del codificatore per configurare un codificatore e archiviare le impostazioni di configurazione. I fornitori del codificatore possono utilizzare l'API del codificatore per esporre le funzionalità di un codificatore. Anche se l'API del codificatore è progettata principalmente per i codificatori, è sufficiente che i decodificatori possano supportarla.

L'API del codificatore viene esposta alle applicazioni tramite l'interfaccia [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) , esposta dal filtro del codificatore. Il filtro del codificatore può essere un filtro DirectShow nativo, un codificatore hardware o un oggetto DMO (DirectX Media Object).

-   Filtri software: un codificatore implementato come filtro DirectShow nativo deve esporre direttamente il [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) .
-   Codificatori hardware: il dispositivo di codifica viene esposto tramite uno o più i Minidriver AVStream, che sono rappresentati in modalità utente da KSProxy. KSProxy converte le chiamate al metodo [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) in set di proprietà KS. Per ulteriori informazioni, vedere la documentazione di DDK.
-   DMOs: DMO deve esporre l'interfaccia [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) . Le applicazioni DirectShow possono eseguire query sul filtro del wrapper DMO, che espone l'interfaccia aggregando DMO. Le applicazioni non basate su DirectShow possono eseguire query direttamente su DMO.

### <a name="encoder-capabilties"></a>Avanzata codificatore

Un codificatore può registrare un elenco di funzionalità di alto livello archiviando tali funzionalità nel registro di sistema. Ogni funzionalità è identificata da un GUID. Per enumerare le funzionalità di un determinato codificatore, eseguire le operazioni seguenti:

1.  Creare il moniker che rappresenta il filtro del codificatore. Vedere [using the System Device Enumerator](using-the-system-device-enumerator.md).
2.  Eseguire una query sul moniker di filtro per l'interfaccia [**IGetCapabilitiesKey**](/windows/desktop/api/Strmif/nn-strmif-igetcapabilitieskey) .
3.  Chiamare [**IGetCapabilitiesKey:: GetCapabilitiesKey**](/windows/desktop/api/Strmif/nf-strmif-igetcapabilitieskey-getcapabilitieskey). Il metodo restituisce un handle per la chiave del registro di sistema che contiene l'elenco delle funzionalità del filtro.
4.  Chiamare la funzione **RegEnumValue** per enumerare i valori per la chiave restituita.

Se si sviluppare un codificatore, creare le voci del registro di sistema per le funzionalità quando il filtro è registrato. Per i filtri software, creare una chiave denominata **funzionalità** adiacente alle chiavi **FilterData** e **FriendlyName** . In genere, è necessario aggiungere queste informazioni dopo aver chiamato [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) per registrare i dati del filtro standard. Per altre informazioni, vedere [How to register DirectShow Filters](how-to-register-directshow-filters.md). In alternativa, è possibile creare una chiave **CapabilitiesLocation** contenente una stringa che fornisce il percorso della chiave delle **funzionalità** nel registro di sistema. La stringa deve iniziare con "HKLM \\ ", "HKCR \\ " o "HKCU \\ " per indicare il sottoalbero del registro di sistema. Per i dispositivi Plug and Play, i file di installazione del driver devono creare una chiave delle **funzionalità** accanto alla chiave **FriendlyName** del filtro oppure usare una chiave **CapabilitiesLocation** come descritto per i filtri software.

Dopo aver creato la chiave delle **funzionalità** , creare un valore per ogni GUID della funzionalità. Il nome del valore deve essere il formato stringa del GUID, nel formato `{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}` . Ogni tipo di valore deve essere uno dei seguenti:

-   Singolo valore numerico. Usare un valore **DWORD** .
-   GUID. Usare il formato stringa del GUID.
-   Coppie numeriche. Usare una stringa con il formato "a, b" per rappresentare coppie di valori, ad esempio larghezza e altezza, o numeratore e denominatore per le frazioni.
-   Matrici di valori. Usare più stringhe (**reg \_ SZ \_ multifunzione**) per rappresentare più di un valore.

Nell'esempio seguente viene illustrato il layout del registro di sistema per un filtro software:


```C++
\HKCR\CLSID\Filter Category\Instance\Filter CLSID\Capabilities\
    
Values: 
    
    guid1: 1234 (REG_DWORD)   
    
    guid2: "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}" (REG_SZ)
    
    guid3: "2","4","6" (REG_SZ_MULTI)
    
    guid4: "720,480" (REG_SZ) 
```



### <a name="encoder-profiles"></a>Profili codificatore

Un *profilo del codificatore* è un elenco fisso di impostazioni di configurazione che possono essere applicate a un codificatore in fase di esecuzione. I profili sono indipendenti dal codificatore; un'applicazione può selezionare un codificatore, quindi selezionare un profilo e applicare le impostazioni del profilo al codificatore. I profili sono identificati dal GUID e devono essere archiviati nel seguente percorso del registro di sistema:


```C++
\HKLM\Software\Microsoft\EncoderProfiles\Profile GUID\
```



*GUID profilo*

formato stringa del GUID che identifica il profilo. Creare valori per ogni impostazione. Creare anche un valore stringa denominato "FriendlyName" i cui dati identificano il profilo, ad esempio "LowBandwidthVideo".

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sviluppo di codificatori e decodificatori](encoder-and-decoder-development.md)
</dt> </dl>

 

 



