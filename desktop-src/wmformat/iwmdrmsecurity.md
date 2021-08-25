---
title: Interfaccia IWMDRMSecurity
description: L'interfaccia IWMDRMSecurity gestisce un'ampia gamma di informazioni relative alla sicurezza per il computer client e il sottosistema DRM (Digital Rights Management). Per ottenere un'istanza di questa interfaccia, chiamare IWMDRMProvider CreateObject.
ms.assetid: 9439aedc-359d-4b2c-a88c-7b0e8eacb5a0
keywords:
- Interfaccia IWMDRMSecurity windows Media Format
- Interfaccia IWMDRMSecurity windows Media Format , descritto
topic_type:
- apiref
api_name:
- IWMDRMSecurity
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 31593dda35e7fa33540faa3c954f1901e1afa227372b25326c0f36154d443153
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839733"
---
# <a name="iwmdrmsecurity-interface"></a>Interfaccia IWMDRMSecurity

**L'interfaccia IWMDRMSecurity** gestisce un'ampia gamma di informazioni relative alla sicurezza per il computer client e il sottosistema DRM (Digital Rights Management).

Per ottenere un'istanza di questa interfaccia, chiamare [**IWMDRMProvider::CreateObject**](iwmdrmprovider-createobject.md). Passare **\_ IWMDRMSecurity IID** come *parametro riid.*

## <a name="members"></a>Membri

**L'interfaccia IWMDRMSecurity** eredita da [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md). **IWMDRMSecurity** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili nell'interfaccia **IWMDRMSecurity.**



| Metodo                                                                                      | Descrizione                                                                                                      |
|:--------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [**CheckCertForRevocation**](iwmdrmsecurity-checkcertforrevocation.md)                     | Determina se un certificato è stato revocato.<br/>                                                    |
| [**GetContentEnablersForRevocations**](iwmdrmsecurity-getcontentenablersforrevocations.md) | Recupera le interfacce di abilitazione del contenuto che consentono il rinnovo dei componenti in base ai certificati revocati.<br/> |
| [**GetContentEnablersFromHashes**](iwmdrmsecurity-getcontentenablersfromhashes.md)         | Recupera le interfacce di abilitazione del contenuto che consentono il rinnovo dei componenti in base a certificati con hash.<br/>  |
| [**GetMachineCertificate**](iwmdrmsecurity-getmachinecertificate.md)                       | Recupera il certificato del computer del sottosistema DRM nel computer client.<br/>                        |
| [**GetRevocationData**](iwmdrmsecurity-getrevocationdata.md)                               | Recupera un elenco di revoche di certificati dall'archivio locale.<br/>                                         |
| [**GetRevocationDataVersion**](iwmdrmsecurity-getrevocationdataversion.md)                 | Recupera il numero di versione di un elenco di revoche di certificati nell'archivio locale.<br/>                     |
| [**GetSecurityVersion**](iwmdrmsecurity-getsecurityversion.md)                             | Recupera la versione del sottosistema DRM nel computer client.<br/>                                    |
| [**PerformSecurityUpdate**](iwmdrmsecurity-performsecurityupdate.md)                       | Avvia un aggiornamento della sicurezza per il sottosistema DRM nel computer client.<br/>                              |
| [**SetRevocationData**](iwmdrmsecurity-setrevocationdata.md)                               | Imposta un elenco di revoche di certificati nell'archivio locale.<br/>                                                |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Esempio di individualizzazione DRM**](drm-individualization-example.md)
</dt> <dt>

[**Interfacce**](drm-interfaces.md)
</dt> <dt>

[**IWMDRMEventGenerator**](iwmdrmeventgenerator.md)
</dt> </dl>

 

 





