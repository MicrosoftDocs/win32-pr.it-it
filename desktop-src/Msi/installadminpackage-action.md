---
description: L'azione InstallAdminPackage copia il database del prodotto nel punto di installazione amministrativa, definito dalla proprietà TARGETDIR.
ms.assetid: 9781f14b-0264-4d00-9a83-bd5400c614ec
title: Azione InstallAdminPackage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1eb2f86390fe3a47a6d100a887d34798e7f4d4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967248"
---
# <a name="installadminpackage-action"></a>Azione InstallAdminPackage

L'azione InstallAdminPackage copia il database del prodotto nel punto di installazione amministrativa, definito dalla proprietà [**targetdir**](targetdir.md) .

## <a name="sequence-restrictions"></a>Restrizioni sequenza

Non esistono restrizioni di sequenza.

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione                                 |
|-------|------------------------------------------------------------|
| \[1\] | Nome dei file di installazione.                                     |
| \[6\] | Dimensioni del database.                                          |
| \[9\] | Identificatore dell'installazione amministrativa: directory del punto. |



 

## <a name="remarks"></a>Commenti

L'azione InstallAdminPackage aggiorna inoltre le informazioni di riepilogo del database e rimuove tutti i file CAB presenti nei flussi dopo la copia del database.

 

 



