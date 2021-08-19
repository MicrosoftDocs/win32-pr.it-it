---
title: Proprietà Caption (oggetto raccolta Commands)
description: Informazioni sulla proprietà Caption dell'oggetto Command Collection. Microsoft Agent è deprecato a Windows 7.
ms.assetid: 7182c21e-1ff0-4dce-9571-534b7576c082
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3467543de127bf0d9e898273f68d4cb921b7ab88ef52e965d73be4c1b465786
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976701"
---
# <a name="caption-property-commands-collection-object"></a>Proprietà Caption (oggetto raccolta Commands)

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Determina il testo visualizzato per [**un oggetto Commands**](/windows/desktop/lwef/the-commands-collection-object) nel menu a comparsa del carattere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agent***. Caratteri ("**_CharacterID_*_")._ * [Stringa Commands.Caption](caption-property.md) \[  =  \]



| Parte     | Descrizione                                                              |
|----------|--------------------------------------------------------------------------|
| *string* | Espressione stringa che restituisce il testo visualizzato come didascalia. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

L'impostazione della proprietà [**Caption**](caption-property.md) per la raccolta [**Commands**](/windows/desktop/lwef/the-commands-collection-object) definisce come verrà visualizzato nel menu a comparsa del carattere quando la relativa proprietà [**Visible**](visible-property.md) è impostata su True e l'applicazione non è il client attivo per l'input. Per specificare un tasto di scelta (unlined mnemonic) per **caption,** includere un carattere e commerciale (&) prima di tale carattere.

Se si definiscono comandi per una [**raccolta Commands**](/windows/desktop/lwef/the-commands-collection-object) con [**una didascalia**](caption-property.md), in genere si definisce anche **una didascalia** per la raccolta **Commands** associata.

 

 
