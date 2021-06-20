---
title: Proprietà Enabled (oggetto Balloon)
description: Informazioni sulla proprietà dell'oggetto Enabled Balloon. Microsoft Agent è deprecato a livello di Windows 7.
ms.assetid: 4d73acda-6fcc-4912-a466-570849aeb807
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 602d39a9bef7713a92707d8a43050f04a3577b6d
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407304"
---
# <a name="enabled-property-balloon-object"></a>Proprietà Enabled (oggetto Balloon)

\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce un valore che indica se il fumetto è abilitato per il carattere specificato.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agent***. Caratteri ("**_CharacterID_*_"). Balloon.Enabled_*



| Valore     | Descrizione              |
|-----------|--------------------------|
| **True**  | Il balloon è abilitato.  |
| **False** | Il balloon è disabilitato. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

La **proprietà Enabled** restituisce un valore booleano che specifica se il balloon è abilitato. Lo stato predefinito del fumetto viene impostato come parte della definizione di un carattere quando il carattere viene compilato nell'editor di caratteri di Microsoft Agent. Se un carattere è definito per non supportare il fumetto, questa proprietà sarà sempre **False** per il carattere.

 

 




