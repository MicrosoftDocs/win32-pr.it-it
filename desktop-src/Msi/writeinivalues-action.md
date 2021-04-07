---
description: L'azione WriteIniValues scrive le informazioni sul file ini che l'applicazione deve scrivere nei relativi file ini.
ms.assetid: ec54db54-293c-4db3-81af-6e8669f27310
title: Azione WriteIniValues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd96e86c361c7fe83b6ad33959149e82fb9d7969
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882693"
---
# <a name="writeinivalues-action"></a>Azione WriteIniValues

L'azione WriteIniValues scrive le informazioni sul file ini che l'applicazione deve scrivere nei relativi file ini. La scrittura di queste informazioni viene gestita dalla tabella dei [componenti](component-table.md). Viene scritto un valore ini se il componente corrispondente è stato impostato per essere installato localmente o eseguito dall'origine.

## <a name="sequence-restrictions"></a>Restrizioni sequenza

L'azione InstallValidate deve precedere l'azione WriteIniValues. Se è presente un' [azione RemoveIniValues](removeinivalues-action.md) nella sequenza, è necessario che venga eseguita prima dell'azione WriteIniValues.

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione              |
|-------|-----------------------------------------|
| \[1\] | Identificatore del file ini.                |
| \[2\] | chiave del file ini nella sezione seguente. |
| \[3\] | Elemento rimosso dal file ini.            |
| \[4\] | Valore rimosso dal file ini.           |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tabella IniFile](inifile-table.md)
</dt> </dl>

 

 



