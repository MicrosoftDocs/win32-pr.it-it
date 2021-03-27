---
description: Implementato dalla Shell per consentire agli sviluppatori di script e Microsoft Visual Basic di usare alcune delle funzionalità disponibili nella shell. L'oggetto ShellUIHelper non dispone di proprietà o eventi. Sono disponibili metodi per aggiungere elementi alla Shell.
title: Oggetto ShellUIHelper (Exdisp. h)
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
ms.openlocfilehash: f0df3b02624a802c19663b67cbcab508c3e0e487
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980719"
---
# <a name="shelluihelper-object"></a>Oggetto ShellUIHelper

Implementato dalla Shell per consentire agli sviluppatori di script e Microsoft Visual Basic di usare alcune delle funzionalità disponibili nella shell. L'oggetto **ShellUIHelper** non dispone di proprietà o eventi. Sono disponibili metodi per aggiungere elementi alla Shell.

## <a name="members"></a>Membri

L'oggetto **ShellUIHelper** dispone di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'oggetto **ShellUIHelper** dispone di questi metodi.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Metodo</th>
<th style="text-align: left;">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="shelluihelper-addchannel.md"><strong>AddChannel</strong></a></td>
<td style="text-align: left;">Consente di aggiungere un nuovo canale all'elenco di canali nel menu <strong>Preferiti</strong> di Internet Explorer e alla barra del <strong>canale</strong> sul desktop.<br/>
<blockquote>
[!Note]<br />
Questo metodo non è più supportato in Windows Vista. In tale sistema operativo restituisce E_NOTIMPL.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shelluihelper-adddesktopcomponent.md"><strong>AddDesktopComponent</strong></a></td>
<td style="text-align: left;">Aggiunge un elemento al desktop attivo.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shelluihelper-addfavorite.md"><strong>AddFavorite</strong></a></td>
<td style="text-align: left;">Visualizza l'interfaccia utente predefinita per la creazione di un elemento preferito. L'interfaccia utente viene inizializzata sui parametri specificati.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shelluihelper-issubscribed.md"><strong>IsSubscribed</strong></a></td>
<td style="text-align: left;">Indica se un URL specificato è sottoscritto.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>                                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>Exdisp. h</dt> </dl>                            |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 4,71 o successiva)</dt> </dl> |



 

 




