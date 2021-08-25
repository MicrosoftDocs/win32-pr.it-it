---
description: L'azione PublishComponents gestisce l'annuncio dei componenti dalla tabella PublishComponent.
ms.assetid: 58d945d7-7dfb-4752-ae19-7e41caca1de7
title: Azione PublishComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4840035677effff22189c357ad881c9abf2c061b169e4283037ca83df19347d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913121"
---
# <a name="publishcomponents-action"></a>Azione PublishComponents

L'azione PublishComponents gestisce l'annuncio dei componenti dalla [tabella PublishComponent.](publishcomponent-table.md)

## <a name="sequence-restrictions"></a>Restrizioni relative alle sequenze

Non sono presenti restrizioni di sequenza.

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione                                   |
|-------|--------------------------------------------------------------|
| \[1\] | GUID che rappresenta l'ID componente di una funzionalità annunciata. |
| \[2\] | Qualificatore dell'ID componente.                                   |



 

## <a name="remarks"></a>Commenti

L'azione PublishComponents pubblica tutti i componenti della tabella PublishComponents che appartengono alle funzionalità selezionate per l'annuncio o l'installazione.

 

 



