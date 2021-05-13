---
description: Implementato da Shell per consentire agli sviluppatori di script e microsoft Visual Basic di usare alcune delle funzionalità disponibili in Shell. L'oggetto ShellUIHelper non ha proprietà o eventi. Vengono forniti metodi per aggiungere elementi alla shell.
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
ms.openlocfilehash: b77d618c4c772859a9009f3cca761c59df83257a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842432"
---
# <a name="shelluihelper-object"></a>Oggetto ShellUIHelper

Implementato da Shell per consentire agli sviluppatori di script e microsoft Visual Basic di usare alcune delle funzionalità disponibili in Shell. **L'oggetto ShellUIHelper** non ha proprietà o eventi. Vengono forniti metodi per aggiungere elementi alla shell.

## <a name="members"></a>Membri

**L'oggetto ShellUIHelper** ha questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'oggetto ShellUIHelper** dispone di questi metodi.



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
<td style="text-align: left;">Aggiunge un nuovo canale all'elenco di canali nel <strong>menu</strong> Preferiti Internet Explorer canale e alla barra <strong>Dei</strong> canali sul desktop.<br/>
<blockquote>
[!Note]<br />
Questo metodo non è più supportato in Windows Vista. In tale sistema operativo, restituisce E_NOTIMPL.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shelluihelper-adddesktopcomponent.md"><strong>AddDesktopComponent</strong></a></td>
<td style="text-align: left;">Aggiunge un elemento al Active Desktop.<br/></td>
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
| Client minimo supportato<br/> | Windows 2000 Professional, solo app desktop di Windows XP \[\]<br/>                                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>Exdisp.h</dt> </dl>                            |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 4.71 o successiva)</dt> </dl> |



 

 




