---
title: Interfaccia IWMDRMLicense
description: L'interfaccia IWMDRMLicense rappresenta un elenco di una o più licenze.
ms.assetid: afef7f9a-6621-4de7-bd40-3211c5c7ba09
keywords:
- Formato Windows Media Interface IWMDRMLicense
- Interfaccia IWMDRMLicense-formato Windows Media, descritto
topic_type:
- apiref
api_name:
- IWMDRMLicense
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 918154b180ed95dce51224e6340a3ab18f432d18
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473579"
---
# <a name="iwmdrmlicense-interface"></a>Interfaccia IWMDRMLicense

L'interfaccia **IWMDRMLicense** rappresenta un elenco di una o più licenze.

## <a name="members"></a>Membri

L'interfaccia **IWMDRMLicense** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IWMDRMLicense** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IWMDRMLicense** dispone di questi metodi.



| Metodo                                                                                   | Descrizione                                                                                                                                                                                                                        |
|:-----------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CanPersist**](iwmdrmlicense-canpersist.md)                                           | Esegue una query per determinare se la licenza può essere mantenute in un archivio licenze locale.<br/>                                                                                                                                               |
| [**CreateDecryptor**](iwmdrmlicense-createdecryptor.md)                                 | Crea un oggetto di decrittografia utilizzando le impostazioni della licenza corrente.<br/>                                                                                                                                                   |
| [**Al CreateDecryptor**](iwmdrmlicense-createencryptor.md)                                 | Crea un oggetto di crittografia utilizzando le impostazioni della licenza corrente.<br/>                                                                                                                                                  |
| [**CreateSecureDecryptor**](iwmdrmlicense-createsecuredecryptor.md)                     | Crea un oggetto di decrittografia protetto. Il decrittografia sicuro è diverso da quello normale in quanto decrittografa il contenuto e quindi lo crittografa nuovamente in base alle impostazioni specificate nei parametri di questo metodo.<br/> |
| [**GetAnalogVideoRestrictionLevels**](iwmdrmlicense-getanalogvideorestrictionlevels.md) | Recupera tutte le restrizioni video analogiche impostate per la licenza corrente.<br/>                                                                                                                                                     |
| [**Getinclusiving**](iwmdrmlicense-getinclusionlist.md)                               | Recupera l'intero elenco di inclusione per la licenza o la catena di licenze corrente.<br/>                                                                                                                                           |
| [**GetLicense**](iwmdrmlicense-getlicense.md)                                           | Recupera la licenza come dati Extensible Markup Language (XML) o XMR (Extensible Media Rights).<br/>                                                                                                                        |
| [**GetLicenseProperty**](iwmdrmlicense-getlicenseproperty.md)                           | Recupera una proprietà dalla licenza corrente.<br/>                                                                                                                                                                          |
| [**GetNext**](iwmdrmlicense-getnext.md)                                                 | Carica le informazioni relative alla licenza successiva nell'elenco.<br/>                                                                                                                                                               |
| [**GetOutputProtectionLevels**](iwmdrmlicense-getoutputprotectionlevels.md)             | Recupera informazioni su tutti i livelli di protezione dell'output (OPLs) assegnati alla licenza.<br/>                                                                                                                                |
| [**PersistLicense**](iwmdrmlicense-persistlicense.md)                                   | Salva la licenza corrente dall'archivio temporaneo nell'archivio licenze locale permanente.<br/>                                                                                                                              |
| [**ResetEnumeration**](iwmdrmlicense-resetenumeration.md)                               | Reimposta l'elenco di licenze sullo stato originale.<br/>                                                                                                                                                                          |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfacce**](drm-interfaces.md)
</dt> </dl>

 

