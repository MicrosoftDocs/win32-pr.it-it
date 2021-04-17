---
title: Registrazione del servizio di testo
description: Oltre alle voci del registro di sistema COM standard del server in-process, un servizio di testo deve registrarsi con il Framework di servizi di testo (TSF), in modo che possa essere usato con un'applicazione.
ms.assetid: 95676067-ab5c-470b-a4be-117ab6810d48
keywords:
- Framework servizi di testo (TSF), registrazione
- TSF (Framework di servizi di testo), registrazione
- Servizi di testo, registrazione
- Framework servizi di testo (TSF), profili linguaggio
- TSF (Framework dei servizi di testo), profili di linguaggio
- Servizi di testo, profili di linguaggio
- Framework servizi di testo (TSF), categorie
- TSF (Framework di servizi di testo), categorie
- Servizi di testo, categorie
- registrazione di servizi di testo
- registrazione dei profili di linguaggio
- registrazione di categorie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45dc1b91ad1a3b1fde9a2e49b92950ce2db4876f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473627"
---
# <a name="text-service-registration"></a>Registrazione del servizio di testo

Oltre alle voci del registro di sistema COM standard del server in-process, un servizio di testo deve registrarsi con il Framework di servizi di testo (TSF), in modo che possa essere usato con un'applicazione. TSF fornisce l'interfaccia [ITfInputProcessorProfiles](/windows/desktop/api/msctf/nn-msctf-itfinputprocessorprofiles) e [ITfCategoryMgr](/windows/desktop/api/msctf/nn-msctf-itfcategorymgr) per semplificare il processo di registrazione.

I provider di servizi di testo devono inoltre fornire firme digitali con i rispettivi file eseguibili binari. Vedere [Introduzione alla firma del codice](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)).

## <a name="registering-the-text-service"></a>Registrazione del servizio di testo

Un servizio di testo si registra con TSF chiamando [ITfInputProcessorProfiles:: Register](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-register) con l'identificatore di classe del servizio di testo. Un'istanza dell'interfaccia **ITfInputProcessorProfiles** viene ottenuta chiamando **CoCreateInstance** con CLSID \_ tf \_ InputProcessorProfiles.

Nell'esempio seguente viene illustrato come creare un oggetto **ITfInputProcessorProfiles** e registrare il servizio di testo.


```C++
BOOL RegisterTextService(CLSID clsidTextService)
{
    HRESULT hr;
    ITfInputProcessorProfiles *pInputProcessProfiles;

    hr = CoCreateInstance(  CLSID_TF_InputProcessorProfiles, 
                            NULL, 
                            CLSCTX_INPROC_SERVER,
                            IID_ITfInputProcessorProfiles, 
                            (LPVOID*)&pInputProcessProfiles);

    if (hr != S_OK)
    {
        return FALSE;
    }

    hr = pInputProcessProfiles->Register(clsidTextService);

    pInputProcessProfiles->Release();
    
    return (S_OK == hr);
}
```



[ITfInputProcessorProfiles:: Annulla registrazione](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-unregister)

## <a name="registering-language-profiles"></a>Registrazione dei profili di linguaggio

Un servizio di testo è disponibile solo quando un'applicazione ha lo stato attivo e la lingua corretta è selezionata nella barra della lingua. Per semplificare questa operazione, TSF richiede che un servizio di testo si registri per tutte le lingue supportate. Il servizio di testo registra i profili di linguaggio chiamando [ITfInputProcessorProfiles:: AddLanguageProfile](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-addlanguageprofile) con l'identificatore della classe del servizio di testo, l'identificatore di lingua del profilo e un **GUID** definito dal servizio di testo che identifica il profilo del linguaggio.

È possibile rimuovere un profilo del linguaggio chiamando [ITfInputProcessorProfiles:: RemoveLanguageProfile](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-removelanguageprofile). **ITfInputProcessorProfiles:: Unregister** rimuove tutti i profili di linguaggio per il servizio di testo; Quando viene disinstallato, un servizio di testo richiede la rimozione dei singoli profili di linguaggio.

## <a name="registering-categories"></a>Registrazione di categorie

Un servizio di testo deve inoltre registrare la categoria a cui si applica il servizio di testo. Se, ad esempio, il servizio di testo fornisce informazioni sugli attributi di visualizzazione, è necessario registrarsi come provider di attributi di visualizzazione chiamando [ITfCategoryMgr:: RegisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory) con l'identificatore di classe del servizio di testo per il primo parametro, GUID \_ TFCAT \_ DISPLAYATTRIBUTEPROVIDER per il secondo parametro e l'identificatore di classe del servizio di testo per il terzo parametro. Le categorie possibili sono elencate in [valori di categoria predefiniti](predefined-category-values.md).

Rimuovere le categorie registrate in precedenza chiamando [ITfCategoryMgr:: UnregisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-unregistercategory). ITfInputProcessorProfiles:: Unregister rimuove tutte le categorie per il servizio di testo; Quando viene disinstallato un servizio di testo, è necessario rimuovere le singole categorie.

 

 