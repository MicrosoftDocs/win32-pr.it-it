---
title: Utilizzo dei profili di sistema localizzati
description: Utilizzo dei profili di sistema localizzati
ms.assetid: d911baf6-0731-4f02-9001-d04464a03f56
keywords:
- profili, sistema
- profili di sistema, localizzati
- profili di sistema, interfaccia IWMProfileManagerLanguage
- profili di sistema localizzati, informazioni
- IWMProfileManagerLanguage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd8c040d9804cd822b17e7caad8a8cfb5e5854c4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299395"
---
# <a name="working-with-localized-system-profiles"></a>Utilizzo dei profili di sistema localizzati

Windows Media Format SDK include i profili di sistema con nomi e descrizioni in diverse lingue. I file con estensione prx del profilo di sistema localizzati vengono installati nella \[ \] \\ cartella sdkroot WMSDK \\ WMFSDK9 \\ LocalizedProfiles Per accedere a un file specifico con i metodi **IWMProfileManagerLanguage** , è necessario spostarlo nella directory radice del sistema insieme agli altri file del profilo di sistema. Per un elenco dei file del profilo di sistema localizzati, vedere [profili di sistema localizzati](localized-system-profiles.md).

È possibile impostare o recuperare il linguaggio del profilo di sistema utilizzando i metodi dell'interfaccia [**IWMProfileManagerLanguage**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanagerlanguage) . Il linguaggio viene specificato come valore LANGID, che è costituito da un identificatore di lingua principale e un identificatore della lingua secondaria. Nel codice seguente viene illustrato come recuperare il linguaggio corrente. La lingua predefinita è U.S. English (0x409). Per ulteriori informazioni sull'utilizzo di questo codice, vedere [utilizzo degli esempi di codice](using-the-code-examples.md).


```C++
HRESULT GetCurrentSystemProfileLanguage(IMWProfilManager* pProfileMgr)
{
    HRESULT hr = S_OK;

    IWMProfileManagerLanguage* pProfileMgrLang = NULL;

    // Get the profile manager language interface.
    hr = pProfileMgr->QueryInterface(IID_IWMProfileManagerLanguage,
                                     (void **) &pProfileMgrLang);
    if(FAILED(hr))
    {
        printf("Couldn't get IWMProfileManagerLanguage.\n");
        SAFE_RELEASE(pProfileMgrLang);
        return hr;
    }

    // Retrieve the current language (as a LANGID value)
    WORD wLangID = 0;
    hr = pProfileMgrLang->GetUserLanguageID(&wLangID);
    if(FAILED(hr))
    {
        printf("Could not get the current language.\n");
        SAFE_RELEASE(pProfileMgrLang);
        return hr;
    }

    printf("The current language ID is 0x%X\n", wLangID);

    SAFE_RELEASE(pProfileMgrLang);
    return S_OK;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Uso dei profili di sistema**](using-system-profiles.md)
</dt> </dl>

 

 




