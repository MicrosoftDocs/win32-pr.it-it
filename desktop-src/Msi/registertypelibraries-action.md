---
description: L'azione RegisterTypeLibraries registra le librerie dei tipi con il sistema. Questa azione viene applicata a ogni file a cui si fa riferimento nella tabella TypeLib pianificata per l'installazione.
ms.assetid: 374450bb-316c-4fe6-abb1-cd8a8a31f284
title: Azione RegisterTypeLibraries
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 469cc18fc2842a3258804fc012c48a49085f1598
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311706"
---
# <a name="registertypelibraries-action"></a>Azione RegisterTypeLibraries

L'azione RegisterTypeLibraries registra le librerie dei tipi con il sistema. Questa azione viene applicata a ogni file a cui si fa riferimento nella [tabella TypeLib](typelib-table.md) pianificata per l'installazione.

## <a name="sequence-restrictions"></a>Restrizioni sequenza

L'azione RegisterTypeLibraries deve essere successiva all'azione [InstallFiles](installfiles-action.md) .

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione                   |
|-------|----------------------------------------------|
| \[1\] | [GUID](guid.md) della libreria dei tipi registrati. |



 

## <a name="remarks"></a>Commenti

Per l'azione RegisterTypeLibraries è necessario che il linguaggio della libreria dei tipi venga creato correttamente nel campo Language della tabella TypeLib. Una modifica errata del campo del linguaggio può causare la mancata registrazione di una libreria dei tipi altrimenti valida nel programma di installazione.

 

 



