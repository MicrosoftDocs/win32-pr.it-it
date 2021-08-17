---
title: Proprietà Enabled (oggetto Balloon)
description: Informazioni sulla proprietà dell'oggetto Balloon abilitato. Microsoft Agent è deprecato a Windows 7.
ms.assetid: 4d73acda-6fcc-4912-a466-570849aeb807
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0d4eaa09e173d847e9dead1bbd559b59e2d12a2d40b5f1d1f989d3cf70263ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118752003"
---
# <a name="enabled-property-balloon-object"></a>Proprietà Enabled (oggetto Balloon)

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce un valore che indica se il fumetto di parole è abilitato per il carattere specificato.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agent***. Caratteri ("**_CharacterID_*_"). Balloon.Enabled_*



| Valore     | Descrizione              |
|-----------|--------------------------|
| **True**  | Il fumetto è abilitato.  |
| **False** | Il fumetto è disabilitato. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

La **proprietà Enabled** restituisce un valore booleano che specifica se il fumetto è abilitato. Lo stato predefinito del fumetto di parole viene impostato come parte della definizione di un carattere quando il carattere viene compilato nell'editor di caratteri di Microsoft Agent. Se un carattere viene definito per non supportare il fumetto di parole, questa proprietà sarà sempre **False** per il carattere.

 

 




