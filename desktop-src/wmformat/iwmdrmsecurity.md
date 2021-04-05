---
title: Interfaccia IWMDRMSecurity
description: L'interfaccia IWMDRMSecurity gestisce un'ampia gamma di informazioni relative alla sicurezza per il computer client e il sottosistema di Digital Rights Management (DRM). Per ottenere un'istanza di questa interfaccia, chiamare IWMDRMProvider CreateObject.
ms.assetid: 9439aedc-359d-4b2c-a88c-7b0e8eacb5a0
keywords:
- Formato Windows Media Interface IWMDRMSecurity
- Interfaccia IWMDRMSecurity-formato Windows Media, descritto
topic_type:
- apiref
api_name:
- IWMDRMSecurity
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d8b18e56c24fd0f3d3f86f217f547d626b74ded0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104334300"
---
# <a name="iwmdrmsecurity-interface"></a>Interfaccia IWMDRMSecurity

L'interfaccia **IWMDRMSecurity** gestisce un'ampia gamma di informazioni relative alla sicurezza per il computer client e il sottosistema di Digital Rights Management (DRM).

Per ottenere un'istanza di questa interfaccia, chiamare [**IWMDRMProvider:: CreateObject**](iwmdrmprovider-createobject.md). Passare **IID \_ IWMDRMSecurity** come parametro *riid* .

## <a name="members"></a>Membri

L'interfaccia **IWMDRMSecurity** eredita da [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md). **IWMDRMSecurity** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IWMDRMSecurity** dispone di questi metodi.



| Metodo                                                                                      | Descrizione                                                                                                      |
|:--------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [**CheckCertForRevocation**](iwmdrmsecurity-checkcertforrevocation.md)                     | Determina se un certificato è stato revocato.<br/>                                                    |
| [**GetContentEnablersForRevocations**](iwmdrmsecurity-getcontentenablersforrevocations.md) | Recupera le interfacce di attivazione del contenuto che consentono il rinnovo dei componenti in base ai certificati revocati.<br/> |
| [**GetContentEnablersFromHashes**](iwmdrmsecurity-getcontentenablersfromhashes.md)         | Recupera le interfacce di attivazione del contenuto che consentono il rinnovo dei componenti in base ai certificati con hash.<br/>  |
| [**GetMachineCertificate**](iwmdrmsecurity-getmachinecertificate.md)                       | Recupera il certificato del computer del sottosistema DRM nel computer client.<br/>                        |
| [**GetRevocationData**](iwmdrmsecurity-getrevocationdata.md)                               | Recupera un elenco di revoche di certificati dall'archivio locale.<br/>                                         |
| [**GetRevocationDataVersion**](iwmdrmsecurity-getrevocationdataversion.md)                 | Recupera il numero di versione di un elenco di revoche di certificati nell'archivio locale.<br/>                     |
| [**GetSecurityVersion**](iwmdrmsecurity-getsecurityversion.md)                             | Recupera la versione del sottosistema DRM nel computer client.<br/>                                    |
| [**PerformSecurityUpdate**](iwmdrmsecurity-performsecurityupdate.md)                       | Avvia un aggiornamento della sicurezza del sottosistema DRM nel computer client.<br/>                              |
| [**SetRevocationData**](iwmdrmsecurity-setrevocationdata.md)                               | Imposta un elenco di revoche di certificati nell'archivio locale.<br/>                                                |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Esempio di individualizzazione DRM**](drm-individualization-example.md)
</dt> <dt>

[**Interfacce**](drm-interfaces.md)
</dt> <dt>

[**IWMDRMEventGenerator**](iwmdrmeventgenerator.md)
</dt> </dl>

 

 





