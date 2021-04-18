---
title: Proprietà Enabled (oggetto Balloon)
description: Proprietà Enabled
ms.assetid: 4d73acda-6fcc-4912-a466-570849aeb807
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07179390b183e98a5eaccb2dfdb4405525d7d26e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300830"
---
# <a name="enabled-property-balloon-object"></a>Proprietà Enabled (oggetto Balloon)

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce un valore che indica se la parola Balloon è abilitata per il carattere specificato.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agente ***. Caratteri ("**_CharacterID_*_"). Balloon. Enabled_*



| Valore     | Descrizione              |
|-----------|--------------------------|
| **True**  | Il fumetto è abilitato.  |
| **False** | Il fumetto è disabilitato. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

La proprietà **Enabled** restituisce un valore booleano che specifica se il fumetto è abilitato. Lo stato predefinito del fumetto di Word viene impostato come parte della definizione di un carattere quando il carattere viene compilato nell'editor dei caratteri di Microsoft Agent. Se un carattere è definito in modo da non supportare la parola Balloon, questa proprietà sarà sempre **false** per il carattere.

 

 




