---
title: Remove (metodo)
description: Remove (metodo)
ms.assetid: b50d47b2-a425-4545-8d85-efeae460d2b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52f7fc80954a1ffe218ba38405a551e5f000dc76
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337478"
---
# <a name="remove-method"></a>Remove (metodo)

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Rimuove un oggetto [**Command**](/windows/desktop/lwef/the-command-object) dalla raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) .

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agente ***. Caratteri ("*** CharacterID ***"). Comandi. Rimuovi*** nome*



| Parte   | Descrizione                                                       |
|--------|-------------------------------------------------------------------|
| *Nome* | Obbligatorio. Valore stringa corrispondente all'ID per il comando. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando un oggetto [**comando**](/windows/desktop/lwef/the-command-object) viene rimosso dalla raccolta, non viene più visualizzato quando il menu popup del carattere viene visualizzato o nella finestra comandi quando l'applicazione client è di input-attivo.

## <a name="see-also"></a>Vedere anche

[**RemoveAll, metodo**](removeall-method.md)


 

 