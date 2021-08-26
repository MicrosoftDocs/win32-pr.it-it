---
description: Implementato dalla shell per consentire agli sviluppatori di script Visual Basic Microsoft di usare alcune delle funzionalità disponibili nella shell. L'oggetto ShellUIHelper non ha proprietà o eventi. Vengono forniti metodi per aggiungere elementi alla shell.
title: Oggetto ShellUIHelper (Exdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellUIHelper
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 9fffebc8-29b9-4064-b60c-c8c63690a79e
ms.openlocfilehash: f254bd218024b3d1df15a826da701b1f010ae616
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473327"
---
# <a name="shelluihelper-object"></a>Oggetto ShellUIHelper

Implementato dalla shell per consentire agli sviluppatori di script Visual Basic Microsoft di usare alcune delle funzionalità disponibili nella shell. **L'oggetto ShellUIHelper** non ha proprietà o eventi. Vengono forniti metodi per aggiungere elementi alla shell.

## <a name="members"></a>Membri

**L'oggetto ShellUIHelper** ha questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'oggetto ShellUIHelper** dispone di questi metodi.




| Metodo | Descrizione | 
|--------|-------------|
| <a href="shelluihelper-addchannel.md"><strong>AddChannel</strong></a> | Aggiunge un nuovo canale all'elenco dei canali nel <strong>menu</strong> <strong></strong> Internet Explorer Preferiti e alla barra dei canali sul desktop.<br /><blockquote>[!Note]<br />Questo metodo non è più supportato in Windows Vista. In tale sistema operativo, restituisce E_NOTIMPL.</blockquote><br /> | 
| <a href="shelluihelper-adddesktopcomponent.md"><strong>AddDesktopComponent</strong></a> | Aggiunge un elemento alla Active Desktop.<br /> | 
| <a href="shelluihelper-addfavorite.md"><strong>AddFavorite</strong></a> | Visualizza l'interfaccia utente predefinita per la creazione di un elemento preferito. L'interfaccia utente viene inizializzata con i parametri specificati.<br /> | 
| <a href="shelluihelper-issubscribed.md"><strong>IsSubscribed</strong></a> | Indica se un URL specificato è sottoscritto.<br /> | 




 

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app desktop XP \[\]<br/>                                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>Exdisp.h</dt> </dl>                            |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 4.71 o successiva)</dt> </dl> |



 

 




