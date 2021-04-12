---
title: Verifica e inizializzazione
description: Verifica e inizializzazione
ms.assetid: e92abaa2-0bac-4c78-bda7-d118c4f5b332
keywords:
- Windows Media Format SDK, verifica
- Windows Media Format SDK, inizializzazione
- Digital Rights Management (DRM), verifica
- DRM (Digital Rights Management), verifica
- Digital Rights Management (DRM), inizializzazione
- DRM (Digital Rights Management), inizializzazione
- API estese del client DRM, verifica
- API estese client, verifica
- API estese del client DRM, inizializzazione
- API estese client, inizializzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59c54b56e0622fb65a1a57ae1909e0e6e64aaca6
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104336377"
---
# <a name="verification-and-initialization"></a>Verifica e inizializzazione

È necessario eseguire la procedura seguente per verificare che la transcrittografia sia consentita e inizializzare un oggetto che definirà il contenuto:

1.  Se si dispone già dell'ID chiave per il contenuto, andare al passaggio 5.
2.  Chiamare la funzione [**WMCreateEditor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateeditor) per creare un oggetto dell'editor di metadati e ottenere un'istanza dell'interfaccia [**IWMMetadataEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor) di tale oggetto.
3.  Chiamare **IWMMetadataEditor:: QueryInterface** per ottenere un'istanza dell'interfaccia [**IWMDRMEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor) .
4.  Chiamare [**IWMDRMEditor:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmeditor-getdrmproperty) per ottenere la proprietà **DRM \_ DRMHeader \_ keyId** .
5.  Inizializzare le API estese del client Windows Media DRM chiamando la funzione [**WMDRMStartup**](wmdrmstartup.md) .
6.  Chiamare la funzione [**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md) per creare un oggetto provider protetto e ottenere un'istanza dell'interfaccia [**IWMDRMProvider**](iwmdrmprovider.md) di tale oggetto.
7.  Chiamare [**IWMDRMProvider:: CreateObject**](iwmdrmprovider-createobject.md) per creare un oggetto di gestione delle licenze e ottenere un'istanza della relativa interfaccia [**IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md) .
8.  Chiamare [**IWMDRMLicenseManagement:: CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md), passando l'ID chiave e il diritto che governa le azioni da intraprendere con il contenuto dopo che è stato transcripto. Questa chiamata recupererà un'istanza dell'interfaccia [**IWMDRMLicense**](iwmdrmlicense.md) che può essere utilizzata per enumerare tutte le licenze corrispondenti.
9.  Chiamare [**IWMDRMLicense:: Getinclusionname**](iwmdrmlicense-getinclusionlist.md) per recuperare l'elenco dei sistemi di protezione del contenuto (CPS) autorizzati come specificato dall'emittente della licenza.
10. Analizzare l'elenco di inclusione per verificare che il GUID del CPS di output sia consentito dalla licenza.
11. Se il GUID di esportazione desiderato non è presente nell'elenco di inclusione, chiamare [**IWMDRMLicense:: GetNext**](iwmdrmlicense-getnext.md) per ottenere la licenza applicabile successiva, se presente, e ripetere i passaggi 9 e 10. Se nessuna licenza dispone del GUID desiderato nell'elenco di inclusione, non è possibile eseguire l'esportazione.
12. Chiamare [**IWMDRMLicense:: CreateSecureDecryptor**](iwmdrmlicense-createsecuredecryptor.md) per creare un oggetto di decrittografia. Passare il certificato dell'applicazione di esportazione. Questa chiamata fornirà un puntatore a un'istanza dell'interfaccia [**IWMDRMDecrypt**](iwmdrmdecrypt.md) dell'oggetto di decrittografia e a un oggetto binario che contiene il valore di inizializzazione. In questo momento solo la costante **RC4 del \_ tipo di protezione \_ \_ DRM** di Windows Media è supportata come argomento al parametro *dwFlags* .
13. Usare lo schema di crittografia RSA OAEP per decrittografare il vettore di inizializzazione.
14. Utilizzare la libreria di analisi ASF fornita da Microsoft quando si immette il contratto di esportazione DRM di Windows Media, per individuare l'offset in byte per ogni payload.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Esportazione di contenuto compresso**](exporting-compressed-content.md)
</dt> </dl>

 

 




