---
description: Espone metodi che consentono le pagine HTML ospitate in un'estensione della procedura guidata per comunicare con la procedura guidata.
ms.assetid: 7b3690dc-2007-43a0-80a3-4a68e3c8464d
title: Oggetto WebWizardHost (shldisp. h)
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
ms.openlocfilehash: 1fbaf53db11fda577e9e9c5384af5f7c62fe1944
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967430"
---
# <a name="webwizardhost-object"></a>Oggetto WebWizardHost

Espone metodi che consentono le pagine HTML ospitate in un'estensione della procedura guidata per comunicare con la procedura guidata.

## <a name="members"></a>Membri

L'oggetto **WebWizardHost** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'oggetto **WebWizardHost** dispone di questi metodi.



| Metodo                                                      | Descrizione                                                                                                                                                                        |
|:------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Annulla**](iwebwizardhost-cancel.md)                     | Simula un clic del pulsante **Annulla** .<br/>                                                                                                                                    |
| [**FinalBack**](iwebwizardhost-finalback.md)               | Passa alla pagina lato client immediatamente precedente alla pagina che ospita le pagine HTML sul lato server.<br/>                                                                    |
| [**FinalNext**](iwebwizardhost-finalnext.md)               | Passa alla pagina della procedura guidata lato client che segue la pagina che ospita le pagine HTML sul lato server oppure termina la procedura guidata se non sono presenti altre pagine lato client.<br/> |
| [**SetHeaderText**](iwebwizardhost-setheadertext.md)       | Imposta il titolo e il sottotitolo visualizzati nell'intestazione della procedura guidata. In generale, il client visualizzerà l'intestazione sopra il codice HTML e sotto la barra del titolo.<br/>                    |
| [**SetWizardButtons**](iwebwizardhost-setwizardbuttons.md) | Aggiorna i pulsanti **indietro**, **Avanti** e **fine** nel frame della procedura guidata del client.<br/>                                                                                    |



 

### <a name="properties"></a>Proprietà

L'oggetto **WebWizardHost** dispone di queste proprietà.



| Proprietà                                               | Tipo di accesso           | Descrizione                                              |
|:-------------------------------------------------------|:----------------------|:---------------------------------------------------------|
| [**Didascalia**](iwebwizardhost-caption.md)<br/>   | Lettura/Scrittura<br/> | Non implementato.<br/>                              |
| [**Proprietà**](iwebwizardhost-property.md)<br/> | Lettura/Scrittura<br/> | Imposta o Recupera il valore corrente di una proprietà.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl> |
| IID<br/>                      | \_WEBWIZARDHOST CLSID<br/>                                                        |



 

 




