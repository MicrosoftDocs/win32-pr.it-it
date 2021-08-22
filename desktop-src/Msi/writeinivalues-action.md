---
description: L'azione WriteIniValues scrive le informazioni .ini file che l'applicazione deve scrivere nei .ini file.
ms.assetid: ec54db54-293c-4db3-81af-6e8669f27310
title: Azione WriteIniValues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce2551725e7b12a697e35b08b403011044bbd631b3ff5bf3d0a5923ecb4c99e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942099"
---
# <a name="writeinivalues-action"></a>Azione WriteIniValues

L'azione WriteIniValues scrive le informazioni .ini file che l'applicazione deve scrivere nei .ini file. La scrittura di queste informazioni è recisa dalla [tabella Component](component-table.md). Un .ini viene scritto se il componente corrispondente è stato impostato per l'installazione locale o l'esecuzione dall'origine.

## <a name="sequence-restrictions"></a>Restrizioni di sequenza

L'azione InstallValidate deve essere eseguita prima dell'azione WriteIniValues. Se è presente [un'azione RemoveIniValues](removeinivalues-action.md) nella sequenza, deve essere eseguita prima dell'azione WriteIniValues.

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione              |
|-------|-----------------------------------------|
| \[1\] | Identificatore del .ini file.                |
| \[2\] | .ini chiave file nella sezione seguente. |
| \[3\] | Elemento rimosso dal .ini file.            |
| \[4\] | Valore rimosso dal .ini file.           |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tabella IniFile](inifile-table.md)
</dt> </dl>

 

 



