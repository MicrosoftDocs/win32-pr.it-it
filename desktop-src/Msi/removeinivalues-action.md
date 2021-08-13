---
description: L'azione RemoveIniValues rimuove le .ini file specificate per la rimozione nella tabella RemoveIniFile se il componente è impostato per l'installazione locale o l'esecuzione dall'origine.
ms.assetid: a30793c8-4154-4990-a42a-d022e69f960a
title: Azione RemoveIniValues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 095985165bf6d9629aa0cae67a5b3f7975d817151ac4b04de40a08d5c2bab4d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118626390"
---
# <a name="removeinivalues-action"></a>Azione RemoveIniValues

L'azione RemoveIniValues rimuove le .ini file specificate per la rimozione nella tabella [RemoveIniFile](removeinifile-table.md) se il componente è impostato per l'installazione locale o l'esecuzione dall'origine. L'azione RemoveIniValues .ini le informazioni sul file associate a un componente nella [tabella IniFile](inifile-table.md). Questa azione rimuove anche .ini file se le informazioni sono state scritte dall'azione [WriteIniValues](writeinivalues-action.md) e se è pianificata la disinstallazione del componente.

## <a name="sequence-restrictions"></a>Restrizioni relative alle sequenze

[L'azione InstallValidate](installvalidate-action.md) deve essere chiamata prima dell'azione RemoveIniValues. Se nella [sequenza viene usata un'azione WriteIniValues,](writeinivalues-action.md) deve essere visualizzata dopo RemoveIniValues.

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione    |
|-------|-------------------------------|
| \[1\] | Identificatore del .ini file.      |
| \[2\] | Sezione .ini chiave del file di configurazione.     |
| \[3\] | Elemento rimosso dal file .ini.  |
| \[4\] | Valore rimosso dal file .ini. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tabella RemoveIniFile](removeinifile-table.md)
</dt> <dt>

[Tabella IniFile](inifile-table.md)
</dt> <dt>

[Azione WriteIniValues](writeinivalues-action.md)
</dt> <dt>

[InstallValidate](installvalidate-action.md)
</dt> </dl>

 

 



