---
description: Se viene impostato questo flag di bit, i tipi di carattere vengono creati utilizzando la tabella codici dell'interfaccia utente predefinita dell'utente. Se il flag di bit non è impostato, i tipi di carattere vengono creati utilizzando la tabella codici del database.
ms.assetid: 6a3dbabe-6a14-4401-b46c-e8a0bd0cbe63
title: Attributo di controllo UsersLanguage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aff4109c5c0819b199343bb8ee38bfecc069ad4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310966"
---
# <a name="userslanguage-control-attribute"></a>Attributo di controllo UsersLanguage

Se viene impostato questo flag di bit, i tipi di carattere vengono creati utilizzando la tabella codici dell'interfaccia utente predefinita dell'utente. Se il flag di bit non è impostato, i tipi di carattere vengono creati utilizzando la tabella codici del database.

## <a name="valid-controls"></a>Controlli validi

[Text](text-control.md)

 

[ListBox](listbox-control.md)

 

[ComboBox](combobox-control.md)

## <a name="value"></a>Valore



| Decimal | Valore esadecimale | Costante                                |
|---------|-------------|-----------------------------------------|
| 1048576 | 0x00100000  | **msidbControlAttributesUsersLanguage** |



 

## <a name="remarks"></a>Commenti

Questo attributo di controllo può essere usato per visualizzare il testo immesso dall'utente in un controllo [Edit](edit-control.md) o [PathEdit](pathedit-control.md) .

Il controllo di modifica, il controllo PathEdit, il [controllo Directory](directorylist-control.md) e il [controllo DirectoryCombo](directorycombo-control.md) utilizzano sempre i tipi di carattere creati nella tabella codici dell'interfaccia utente predefinita dell'utente. Questo può causare problemi se nel sistema operativo sono state installate altre lingue. In questo caso, i tipi di carattere nel computer potrebbero non essere in grado di rappresentare tutti i caratteri nelle lingue aggiunte. Per determinare quali tipi di carattere è possibile usare, cercare i valori in **HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ FontLink \\ SYSTEMLINK**.

Per altre informazioni, vedere [controllare gli attributi](control-attributes.md) e i [controlli](controls.md).

 

 



