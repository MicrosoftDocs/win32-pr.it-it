---
description: L'azione InstallAdminPackage copia il database del prodotto nel punto di installazione amministrativa, definito dalla proprietà TARGETDIR.
ms.assetid: 9781f14b-0264-4d00-9a83-bd5400c614ec
title: Azione InstallAdminPackage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1879d711e1a52a7121326ba170bb3a004fbfb4ee988b35d19a16e1a53c3e2811
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996591"
---
# <a name="installadminpackage-action"></a>Azione InstallAdminPackage

L'azione InstallAdminPackage copia il database del prodotto nel punto di installazione amministrativa, definito dalla [**proprietà TARGETDIR.**](targetdir.md)

## <a name="sequence-restrictions"></a>Restrizioni relative alle sequenze

Non sono presenti restrizioni di sequenza.

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione                                 |
|-------|------------------------------------------------------------|
| \[1\] | Nome dei file di installazione.                                     |
| \[6\] | Dimensioni del database.                                          |
| \[9\] | Identificatore della directory del punto di installazione amministrativa. |



 

## <a name="remarks"></a>Commenti

L'azione InstallAdminPackage aggiorna anche le informazioni di riepilogo del database e rimuove tutti i file CAB presenti nei flussi dopo la copia del database.

 

 



