---
description: L'azione PublishComponents gestisce l'annuncio dei componenti dalla tabella PublishComponent.
ms.assetid: 58d945d7-7dfb-4752-ae19-7e41caca1de7
title: Azione PublishComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9c8967e737193922a9dbc3d9e03bc95131d5a63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881497"
---
# <a name="publishcomponents-action"></a>Azione PublishComponents

L'azione PublishComponents gestisce l'annuncio dei componenti dalla tabella [PublishComponent](publishcomponent-table.md) .

## <a name="sequence-restrictions"></a>Restrizioni sequenza

Non esistono restrizioni di sequenza.

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione                                   |
|-------|--------------------------------------------------------------|
| \[1\] | GUID che rappresenta l'ID componente di una funzionalità annunciata. |
| \[2\] | Qualificatore dell'ID componente.                                   |



 

## <a name="remarks"></a>Commenti

L'azione PublishComponents pubblica tutti i componenti dalla tabella PublishComponents che appartengono alle funzionalità selezionate per l'annuncio o l'installazione.

 

 



