---
title: Metodo Remove
description: Metodo Remove
ms.assetid: b50d47b2-a425-4545-8d85-efeae460d2b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3337fb25db49f1d6c8ccd6d94f2817340db226e14718cfa7943940fbfb069b07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117882782"
---
# <a name="remove-method"></a>Metodo Remove

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Rimuove un [**oggetto Command**](/windows/desktop/lwef/the-command-object) dalla [**raccolta Commands.**](/windows/desktop/lwef/the-commands-collection-object)

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agent***. Caratteri ("**_CharacterID_*_"). Commands.Remove_ * _Name_



| Parte   | Descrizione                                                       |
|--------|-------------------------------------------------------------------|
| *Nome* | Obbligatorio. Valore stringa corrispondente all'ID per il comando. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando un [**oggetto Command**](/windows/desktop/lwef/the-command-object) viene rimosso dalla raccolta, non viene più visualizzato quando viene visualizzato il menu a comparsa del carattere o nella finestra comandi quando l'applicazione client è attiva per l'input.

## <a name="see-also"></a>Vedere anche

[**RemoveAll, metodo**](removeall-method.md)


 

 