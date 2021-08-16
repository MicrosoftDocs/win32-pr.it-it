---
description: L'azione RegisterTypeLibraries registra le librerie dei tipi con il sistema. Questa azione viene applicata a ogni file a cui si fa riferimento nella tabella TypeLib pianificata per l'installazione.
ms.assetid: 374450bb-316c-4fe6-abb1-cd8a8a31f284
title: Azione RegisterTypeLibraries
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac42c831c8413f297d3df2302523a2372b11d1efcffe82ce0d3a82da722832cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118626764"
---
# <a name="registertypelibraries-action"></a>Azione RegisterTypeLibraries

L'azione RegisterTypeLibraries registra le librerie dei tipi con il sistema. Questa azione viene applicata a ogni file a cui si fa riferimento nella [tabella TypeLib](typelib-table.md) pianificata per l'installazione.

## <a name="sequence-restrictions"></a>Restrizioni di sequenza

L'azione RegisterTypeLibraries deve essere eseguita dopo [l'azione InstallFiles.](installfiles-action.md)

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione                   |
|-------|----------------------------------------------|
| \[1\] | [GUID](guid.md) della libreria dei tipi registrata. |



 

## <a name="remarks"></a>Commenti

L'azione RegisterTypeLibraries richiede che il linguaggio della libreria dei tipi sia creato correttamente nel campo Linguaggio della tabella TypeLib. La creazione non corretta del campo Language può causare l'errore del programma di installazione di registrare una libreria dei tipi altrimenti valida.

 

 



