---
title: Interfaccia IWMDRMLicense
description: L'interfaccia IWMDRMLicense rappresenta un elenco di una o più licenze.
ms.assetid: afef7f9a-6621-4de7-bd40-3211c5c7ba09
keywords:
- Formato windows Media dell'interfaccia IWMDRMLicense
- Interfaccia IWMDRMLicense windows Media Format , descritta
topic_type:
- apiref
api_name:
- IWMDRMLicense
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 38aadbda7a0ab6e899e4100adb5ff03873a4dd683fcb8f5893c506033545d558
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117847128"
---
# <a name="iwmdrmlicense-interface"></a>Interfaccia IWMDRMLicense

**L'interfaccia IWMDRMLicense** rappresenta un elenco di una o più licenze.

## <a name="members"></a>Membri

**L'interfaccia IWMDRMLicense** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IWMDRMLicense** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili nell'interfaccia **IWMDRMLicense.**



| Metodo                                                                                   | Descrizione                                                                                                                                                                                                                        |
|:-----------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CanPersist**](iwmdrmlicense-canpersist.md)                                           | Esegue una query per determinare se la licenza può essere mantenuta in un archivio licenze locale.<br/>                                                                                                                                               |
| [**CreateDecryptor**](iwmdrmlicense-createdecryptor.md)                                 | Crea un oggetto di decrittografia usando le impostazioni della licenza corrente.<br/>                                                                                                                                                   |
| [**Createencryptor**](iwmdrmlicense-createencryptor.md)                                 | Crea un oggetto encryptor usando le impostazioni della licenza corrente.<br/>                                                                                                                                                  |
| [**CreateSecureDecryptor**](iwmdrmlicense-createsecuredecryptor.md)                     | Crea un oggetto decrittografia sicuro. Il decrittografo protetto differisce dal normale decrittografatore in quanto decrittografa il contenuto e quindi lo crittografa nuovamente in base alle impostazioni specificate nei parametri di questo metodo.<br/> |
| [**GetAnalogVideoRestrictionLevels**](iwmdrmlicense-getanalogvideorestrictionlevels.md) | Recupera tutte le restrizioni video analogiche impostate per la licenza corrente.<br/>                                                                                                                                                     |
| [**GetInclusionList**](iwmdrmlicense-getinclusionlist.md)                               | Recupera l'intero elenco di inclusione per la licenza o la catena di licenze corrente.<br/>                                                                                                                                           |
| [**GetLicense**](iwmdrmlicense-getlicense.md)                                           | Recupera la licenza come Extensible Markup Language (XML) o Extensible Media Rights (XMR).<br/>                                                                                                                        |
| [**GetLicenseProperty**](iwmdrmlicense-getlicenseproperty.md)                           | Recupera una proprietà dalla licenza corrente.<br/>                                                                                                                                                                          |
| [**Getnext**](iwmdrmlicense-getnext.md)                                                 | Carica le informazioni sulla licenza successiva nell'elenco.<br/>                                                                                                                                                               |
| [**GetOutputProtectionLevels**](iwmdrmlicense-getoutputprotectionlevels.md)             | Recupera informazioni su tutti i livelli di protezione dell'output assegnati alla licenza.<br/>                                                                                                                                |
| [**PersistLicense**](iwmdrmlicense-persistlicense.md)                                   | Salva la licenza corrente dall'archivio temporaneo nell'archivio licenze locale permanente.<br/>                                                                                                                              |
| [**ResetEnumeration**](iwmdrmlicense-resetenumeration.md)                               | Reimposta lo stato originale dell'elenco di licenze.<br/>                                                                                                                                                                          |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfacce**](drm-interfaces.md)
</dt> </dl>

 

