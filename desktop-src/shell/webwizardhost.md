---
description: Espone metodi che consentono alle pagine HTML ospitate in un'estensione della procedura guidata di comunicare con la procedura guidata.
ms.assetid: 7b3690dc-2007-43a0-80a3-4a68e3c8464d
title: Oggetto WebWizardHost (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost
api_type:
- COM
api_location:
- Shldisp.h
ms.openlocfilehash: c5bcf40a77c2f464d5277ac4823ed74a3f3c2bdd6a2114d2431684cc8b319f66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967750"
---
# <a name="webwizardhost-object"></a>Oggetto WebWizardHost

Espone metodi che consentono alle pagine HTML ospitate in un'estensione della procedura guidata di comunicare con la procedura guidata.

## <a name="members"></a>Membri

**L'oggetto WebWizardHost** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'oggetto WebWizardHost** dispone di questi metodi.



| Metodo                                                      | Descrizione                                                                                                                                                                        |
|:------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Annulla**](iwebwizardhost-cancel.md)                     | Simula un clic **sul pulsante** Annulla.<br/>                                                                                                                                    |
| [**FinalBack**](iwebwizardhost-finalback.md)               | Passa alla pagina sul lato client immediatamente precedente alla pagina che ospita le pagine HTML sul lato server.<br/>                                                                    |
| [**FinalNext**](iwebwizardhost-finalnext.md)               | Passa alla pagina della procedura guidata lato client che segue la pagina che ospita le pagine HTML sul lato server o termina la procedura guidata se non sono presenti altre pagine sul lato client.<br/> |
| [**SetHeaderText**](iwebwizardhost-setheadertext.md)       | Imposta il titolo e il sottotitolo visualizzati nell'intestazione della procedura guidata. In generale, il client visualizza l'intestazione sopra il codice HTML e sotto la barra del titolo.<br/>                    |
| [**SetWizardButtons**](iwebwizardhost-setwizardbuttons.md) | Aggiorna i **pulsanti Indietro** **,** Avanti **e** Fine nella cornice della procedura guidata del client.<br/>                                                                                    |



 

### <a name="properties"></a>Proprietà

**L'oggetto WebWizardHost** ha queste proprietà.



| Proprietà                                               | Tipo di accesso           | Descrizione                                              |
|:-------------------------------------------------------|:----------------------|:---------------------------------------------------------|
| [**Didascalia**](iwebwizardhost-caption.md)<br/>   | Lettura/Scrittura<br/> | Non implementato.<br/>                              |
| [**Proprietà**](iwebwizardhost-property.md)<br/> | Lettura/Scrittura<br/> | Imposta o recupera il valore corrente di una proprietà.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                            |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl> |
| IID<br/>                      | CLSID \_ WebWizardHost<br/>                                                        |



 

 




