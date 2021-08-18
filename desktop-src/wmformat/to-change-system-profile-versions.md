---
title: Per modificare le versioni del profilo di sistema
description: Per modificare le versioni del profilo di sistema
ms.assetid: 66bf4041-47b5-41b4-abb4-eb08d05e3b28
keywords:
- profili, sistema
- profili di sistema, versioni
- profili di sistema, modifica delle versioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c963a142c879242b5e2ae734dedb4073a120a57a9121c3f3f95e5838c15110a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119084271"
---
# <a name="to-change-system-profile-versions"></a>Per modificare le versioni del profilo di sistema

Ogni volta che si crea un oggetto di gestione profili, analizza i profili di sistema. È possibile scorrere i profili di sistema usando i metodi [**IWMProfileManager::GetSystemProfileCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-getsystemprofilecount) e [**IWMProfileManager::LoadSystemProfile,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile) ma la gestione profili conta ed elenca solo i profili di una singola versione alla volta. Se si vuole usare questo metodo per trovare i profili di sistema, è necessario assicurarsi che la gestione dei profili si occupi della versione desiderata. Usare i metodi [**dell'interfaccia IWMProfileManager2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager2) per impostare e recuperare la versione del profilo di sistema usata da Gestione profili.

Le versioni vengono specificate usando i membri del tipo [**di enumerazione WMT \_ VERSION.**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_version) Se si imposta la versione del profilo di sistema su WMT \_ VER 9 0, la chiamata avrà esito positivo, ma il numero di profili \_ \_ di sistema sarà zero. Ciò è dovuto al fatto che nessun profilo di sistema predefinito usa Windows codec media audio e video serie 9. Per altre informazioni sull'aggiornamento dei profili per l'uso dei codec più recenti, vedere [Riutilizzo delle configurazioni dei flussi](reusing-stream-configurations.md).

Se si carica un profilo di sistema in base al relativo identificatore GUID, non è importante la versione del profilo di sistema in uso da parte di Gestione profili. Per altre informazioni sul caricamento dei profili di sistema, vedere [Per caricare un profilo di sistema](to-load-a-system-profile.md).

Il codice di esempio seguente illustra come impostare e recuperare la versione del profilo di sistema. Questo esempio usa printf per l'output della console e richiede l'uso di stdio.h. Per altre informazioni sull'uso di questo codice, vedere [Uso degli esempi di codice](using-the-code-examples.md).


```C++
int main(void)
{
    HRESULT hr = S_OK;

    IWMProfileManager*  pProfileMgr  = NULL;
    IWMProfileManager2* pProfileMgr2 = NULL;

    WMT_VERSION         profileVersion;

    // Initialize COM.
    hr = CoInitialize(NULL);
    if(FAILED(hr))
    {
        printf("Could not initialize COM.");
        return 0;
    }

    // Create a profile manager object.
    hr = WMCreateProfileManager(&pProfileMgr);
    if(FAILED(hr))
    {
        printf("Could not create a profile manager object.");
        return 0;
    }

    // Get the IWMProfileManager2 interface.
    hr = pProfileMgr->QueryInterface(IID_IWMProfileManager2, 
                                     (void**) &pProfileMgr2);
    if(FAILED(hr))
    {
        printf("Could not get the IWMProfileManager2 interface.");
        SAFE_RELEASE(pProfileMgr);
        return 0;
    }

    // Release the old interface.
    SAFE_RELEASE(pProfileMgr);

    // Get the current system profile version.
    hr = pProfileMgr2->GetSystemProfileVersion(&profileVersion);
    if(FAILED(hr))
    {
        printf("Could not retrieve profile version.");
        printf("\nError code: 0x%X\n", hr);
        SAFE_RELEASE(pProfileMgr2);
        return 0;
    }
    
    // Display the current version.
    printf("Current version: ");
    switch(profileVersion)
    {
    case WMT_VER_4_0:
        printf("WMT_VER_4_0\n");
        break;
    case WMT_VER_7_0:
        printf("WMT_VER_7_0\n");
        break;
    case WMT_VER_8_0:
        printf("WMT_VER_8_0\n");
        break;
    case WMT_VER_9_0:
        printf("WMT_VER_9_0\n");
        break;
    }

    // Set the system profile version to 8.
    profileVersion = WMT_VER_8_0;

    hr = pProfileMgr2->SetSystemProfileVersion(profileVersion);
    if(FAILED(hr))
    {
        printf("Could not change profile version.");
        printf("\nError code: 0x%X\n", hr);
        SAFE_RELEASE(pProfileMgr2);
        return 0;
    }

    // Print verification.
    printf("Successfully set version to ");
    switch(profileVersion)
    {
    case WMT_VER_4_0:
        printf("WMT_VER_4_0\n");
        break;
    case WMT_VER_7_0:
        printf("WMT_VER_7_0\n");
        break;
    case WMT_VER_8_0:
        printf("WMT_VER_8_0\n");
        break;
    case WMT_VER_9_0:
        printf("WMT_VER_9_0\n");
        break;
    }

    // Clean up.
    SAFE_RELEASE(pProfileMgr2);
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Uso dei profili di sistema**](using-system-profiles.md)
</dt> </dl>

 

 




