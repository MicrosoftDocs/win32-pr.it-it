---
description: L'azione RemoveIniValues rimuove le informazioni sul file ini specificate per la rimozione nella tabella RemoveIniFile se il componente è impostato per essere installato localmente o da Run-from-source.
ms.assetid: a30793c8-4154-4990-a42a-d022e69f960a
title: Azione RemoveIniValues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7dfb847d911e847de00ede6eab30ac3a86615eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968509"
---
# <a name="removeinivalues-action"></a>Azione RemoveIniValues

L'azione RemoveIniValues rimuove le informazioni sul file ini specificate per la rimozione nella [tabella RemoveIniFile](removeinifile-table.md) se il componente è impostato per essere installato localmente o da Run-from-source. L'azione RemoveIniValues rimuove le informazioni sul file ini associate a un componente nella [tabella inifile](inifile-table.md). Questa azione rimuove anche le informazioni sul file ini se le informazioni sono state scritte dall' [azione WriteIniValues](writeinivalues-action.md) e il componente è pianificato per la disinstallazione.

## <a name="sequence-restrictions"></a>Restrizioni sequenza

L'azione [InstallValidate](installvalidate-action.md) deve essere chiamata prima dell'azione RemoveIniValues. Se nella sequenza viene utilizzata un'azione [WriteIniValues](writeinivalues-action.md) , è necessario che venga visualizzata dopo RemoveIniValues.

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione    |
|-------|-------------------------------|
| \[1\] | Identificatore del file ini.      |
| \[2\] | Sezione chiave del file ini.     |
| \[3\] | Elemento rimosso dal file ini.  |
| \[4\] | Valore rimosso dal file ini. |



 

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

 

 



