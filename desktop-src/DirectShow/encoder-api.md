---
description: API del codificatore
ms.assetid: 3d19152f-17a3-4576-a2a2-5b827d9ca8d1
title: API del codificatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b97dc2242cc718605a851186c726e3301493b7637b94e88b7987868741874a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823641"
---
# <a name="encoder-api"></a>API del codificatore

L'API Codificatore fornisce un'interfaccia uniforme per la configurazione di codificatori software e hardware. Le applicazioni possono usare l'API Codificatore per configurare un codificatore e archiviare le impostazioni di configurazione. I fornitori di codificatori possono usare l'API Encoder per esporre le funzionalità di un codificatore. Anche se l'API Codificatore è progettata principalmente per i codificatori, è sufficientemente generale che i decodificatori possano supportarla.

L'API Del codificatore viene esposta alle applicazioni tramite [**l'interfaccia ICodecAPI,**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) esposta dal filtro del codificatore. Il filtro del codificatore può essere un filtro DirectShow nativo, un codificatore hardware o un oggetto directx media (DMO).

-   Filtri software: un codificatore implementato come filtro DirectShow deve esporre direttamente [**ICodecAPI.**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
-   Codificatori hardware: il dispositivo di codifica viene esposto tramite uno o più minidriver AVStream, rappresentati in modalità utente da KSProxy. KSProxy converte le [**chiamate al metodo ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) in set di proprietà KS. Per altre informazioni, vedere la documentazione di DDK.
-   DMO: il DMO deve esporre [**l'interfaccia ICodecAPI.**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) DirectShow applicazioni possono eseguire query sul filtro wrapper DMO, che espone l'interfaccia aggregando il DMO. Le applicazioni non basate su DirectShow possono eseguire query direttamente sul DMO.

### <a name="encoder-capabilties"></a>Capabilties del codificatore

Un codificatore può registrare un elenco di funzionalità di alto livello archiviandole nel Registro di sistema. Ogni funzionalità è identificata da un GUID. Per enumerare le funzionalità di un codificatore specifico, eseguire le operazioni seguenti:

1.  Creare il moniker che rappresenta il filtro del codificatore. Vedere [Uso dell'enumeratore del dispositivo di sistema.](using-the-system-device-enumerator.md)
2.  Eseguire una query sul moniker di filtro per [**l'interfaccia IGetCapabilitiesKey.**](/windows/desktop/api/Strmif/nn-strmif-igetcapabilitieskey)
3.  Chiamare [**IGetCapabilitiesKey::GetCapabilitiesKey**](/windows/desktop/api/Strmif/nf-strmif-igetcapabilitieskey-getcapabilitieskey). Il metodo restituisce un handle alla chiave del Registro di sistema che contiene l'elenco di funzionalità del filtro.
4.  Chiamare la **funzione RegEnumValue** per enumerare i valori per la chiave restituita.

Se si esegue lo sviluppo di un codificatore, creare le voci del Registro di sistema per le funzionalità quando il filtro viene registrato. Per i filtri software, creare una chiave denominata **Capabilities** adiacente alle **chiavi FilterData** **e FriendlyName.** In genere, è necessario aggiungere queste informazioni dopo aver chiamato [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) per registrare i dati di filtro standard. Per altre informazioni, vedere [Come registrare DirectShow filtri](how-to-register-directshow-filters.md). In alternativa, è possibile creare una **chiave CapabilitiesLocation** contenente una stringa che specifica il percorso della chiave **Capabilities** nel Registro di sistema. La stringa deve iniziare con "HKLM", \\ "HKCR" o \\ "HKCU" per \\ indicare il sottoalbero del Registro di sistema. Per Plug and Play dispositivi, i file di installazione del driver devono creare una chiave **Capabilities** adiacente alla chiave **FriendlyName** del filtro oppure usare una **chiave CapabilitiesLocation** come descritto per i filtri software.

Dopo aver creato la chiave **Funzionalità,** creare un valore per ogni GUID di funzionalità. Il nome del valore deve essere il formato stringa del GUID, nel formato `{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}` . Ogni tipo di valore deve essere uno dei seguenti:

-   Singolo valore numerico. Usare un **valore DWORD.**
-   GUID. Usare il formato stringa del GUID.
-   Coppie numeriche. Usare una stringa nel formato "a,b" per rappresentare coppie di valori, ad esempio larghezza e altezza, o numeratore e denominatore per le frazioni.
-   Matrici di valori. Usare più stringhe (**REG \_ SZ \_ MULTI**) per rappresentare più valori.

L'esempio seguente illustra il layout del Registro di sistema per un filtro software:


```C++
\HKCR\CLSID\Filter Category\Instance\Filter CLSID\Capabilities\
    
Values: 
    
    guid1: 1234 (REG_DWORD)   
    
    guid2: "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}" (REG_SZ)
    
    guid3: "2","4","6" (REG_SZ_MULTI)
    
    guid4: "720,480" (REG_SZ) 
```



### <a name="encoder-profiles"></a>Profili del codificatore

Un *profilo codificatore* è un elenco fisso di impostazioni di configurazione che possono essere applicate a un codificatore in fase di esecuzione. I profili sono indipendenti dal codificatore. un'applicazione può selezionare un codificatore, quindi selezionare un profilo e applicare le impostazioni del profilo al codificatore. I profili sono identificati dal GUID e devono essere archiviati nel percorso seguente nel Registro di sistema:


```C++
\HKLM\Software\Microsoft\EncoderProfiles\Profile GUID\
```



dove *GUID del profilo*

è il formato stringa del GUID che identifica il profilo. Creare valori per ogni impostazione. Creare anche un valore stringa denominato "FriendlyName" i cui dati identificano il profilo, ad esempio "LowBandwidthVideo".

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sviluppo di codificatori e decodificatori](encoder-and-decoder-development.md)
</dt> </dl>

 

 



