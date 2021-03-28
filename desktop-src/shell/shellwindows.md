---
description: Rappresenta una raccolta di finestre aperte che appartengono alla Shell. I metodi associati a questi oggetti possono controllare ed eseguire comandi all'interno della shell e ottenere altri oggetti correlati alla Shell.
ms.assetid: cad1f961-7fb4-4ba1-be48-b664d3de2c60
title: Oggetto ShellWindows (Exdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellWindows
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 6a3a782dd4e29d56f5edc7a869004ac7b3fb7ccd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104979810"
---
# <a name="shellwindows-object"></a>Oggetto ShellWindows

Rappresenta una raccolta di finestre aperte che appartengono alla Shell. I metodi associati a questi oggetti possono controllare ed eseguire comandi all'interno della shell e ottenere altri oggetti correlati alla Shell.

## <a name="members"></a>Membri

L'oggetto **ShellWindows** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'oggetto **ShellWindows** dispone di questi metodi.



| Metodo                                                 | Descrizione                                                                                                         |
|:-------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](shellwindows--newenum-method-7ral.md) | Crea e restituisce un nuovo oggetto **ShellWindows** che è una copia di questo oggetto **ShellWindows** .<br/>        |
| [**Elemento**](shellwindows-item.md)                      | Recupera un oggetto [**InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) che rappresenta la finestra della shell.<br/> |



 

### <a name="properties"></a>Proprietà

L'oggetto **ShellWindows** dispone di queste proprietà.



| Proprietà                                       | Tipo di accesso          | Descrizione                                                |
|:-----------------------------------------------|:---------------------|:-----------------------------------------------------------|
| [**Conteggio**](shellwindows-count.md)<br/> | Sola lettura<br/> | Contiene il numero di elementi nella raccolta.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>                                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>Exdisp. h</dt> </dl>                            |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 4,71 o successiva)</dt> </dl> |



 

 
