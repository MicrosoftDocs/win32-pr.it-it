---
title: Proprietà Caption (oggetto raccolta Commands)
description: Proprietà Caption
ms.assetid: 7182c21e-1ff0-4dce-9571-534b7576c082
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2010fe051568f71c4940b4bcf964f257ba9f52ca
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104118794"
---
# <a name="caption-property-commands-collection-object"></a>Proprietà Caption (oggetto raccolta Commands)

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Determina il testo visualizzato per un oggetto [**Commands**](/windows/desktop/lwef/the-commands-collection-object) nel menu popup del carattere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agente ***. Caratteri ("**_CharacterID_*_")._ * [Stringa Commands. Caption](caption-property.md) \[  =  \]



| Parte     | Descrizione                                                              |
|----------|--------------------------------------------------------------------------|
| *string* | Espressione stringa che restituisce il testo visualizzato come didascalia. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

L'impostazione della proprietà [**Caption**](caption-property.md) per la raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) definisce la modalità di visualizzazione nel menu popup del carattere quando la relativa proprietà [**Visible**](visible-property.md) è impostata su true e l'applicazione non è il client di input-Active. Per specificare un tasto di scelta (mnemonico) per la **didascalia**, includere un carattere e commerciale (&) prima di tale carattere.

Se si definiscono comandi per una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) con una [**didascalia**](caption-property.md), in genere si definisce anche una **didascalia** per la raccolta di **comandi** associati.

 

 
