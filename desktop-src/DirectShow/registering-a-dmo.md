---
description: Registrazione di un DMO
ms.assetid: 9f74fc1c-b903-4725-b667-3c56a2726dbc
title: Registrazione di un DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19c5364304fd5f6a9557c84a4b27c86d29fa4e84
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303899"
---
# <a name="registering-a-dmo"></a>Registrazione di un DMO

Per consentire ai client di usare DMO, il CLSID deve essere registrato nel sistema dell'utente. Questa operazione viene eseguita tramite la funzione **DllRegisterServer** della dll. Se si utilizza il Active Template Library (ATL), questa funzione viene generata automaticamente dalla procedura guidata ATL.

È anche possibile registrare il DMO in una o più categorie DMO standard. Questo consente ai client di individuare il DMO usando la funzione [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) . Le categorie sono definite dal GUID e sono elencate nella sezione [GUID DMO](dmo-guids.md).

La registrazione di un DMO in una categoria è facoltativa. A tale scopo, chiamare la funzione [**DMORegister**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoregister) e specificare il nome descrittivo di DMO, il CLSID e la categoria. Facoltativamente, è anche possibile registrare un set di tipi di supporto supportati dal DMOs. Per ulteriori informazioni, vedere [DMO media types](dmo-media-types.md).

Nell'esempio seguente viene illustrato come registrare un valore DMO (audio Effect) che supporta l'input e l'output audio PCM. In questo caso i tipi di input e di output sono uguali.


```C++
STDAPI DllRegisterServer(void)
{
    // Register the DMO as a PCM audio effect DMO
    DMO_PARTIAL_MEDIATYPE mt;
    mt.type    = MEDIATYPE_Audio;
    mt.subtype = MEDIASUBTYPE_PCM;
    HRESULT hr = DMORegister(
        L"MyDMO",                  // Friendly name
        CLSID_MyDMO,               // CLSID
        DMOCATEGORY_AUDIO_EFFECT,  // Category
        0,                         // Flags 
        1,                         // Number of input types
        &mt,                       // Array of input types
        1,                         // Number of output types
        &mt);                      // Array of output types

    if (FAILED(hr)) return hr;

    // Registers the object, with no typelib.
    return _Module.RegisterServer(FALSE);
}
```



In questo esempio si presuppone che ATL sia stato utilizzato per creare il progetto. L'ultima riga della funzione chiama il metodo standard ATL per registrare il server COM. Se non si usa ATL, l'aspetto della funzione sarà diverso.

**Annullamento della registrazione di un DMO**

La funzione **DllUnregisterServer** deve rimuovere qualsiasi voce del registro di sistema creata dalla funzione **DllRegisterServer** . Se si chiama **DMORegister** quando si registra DMO, è necessario [**DMOUnregister**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmounregister) con la stessa categoria quando si annulla la registrazione di DMO.

Nell'esempio seguente vengono rimosse le voci del registro di sistema create nell'esempio precedente:


```C++
STDAPI DllUnregisterServer(void)
{
    DMOUnregister(CLSID_MyDMO, DMOCATEGORY_AUDIO_EFFECT);
    return _Module.UnregisterServer(TRUE);
}
```



**Valori Merit di DirectShow**

Ai fini della creazione di grafici di filtro, DirectShow assegna un valore Merit predefinito a DMOs. È possibile eseguire l'override di questo valore aggiungendo una voce del registro di sistema alla chiave del registro di sistema DMO nel \_ CLSID radice delle classi HKEY \_ \\ . Includere un valore **DWORD** denominato `Merit` il cui valore specifichi il merito.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scrittura di un DMO](writing-a-dmo.md)
</dt> </dl>

 

 



