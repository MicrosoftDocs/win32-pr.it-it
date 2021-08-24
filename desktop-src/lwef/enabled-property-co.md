---
title: Proprietà Enabled (oggetto Command)
description: Informazioni sulla proprietà dell'oggetto Comando abilitato. Microsoft Agent è deprecato a Windows 7.
ms.assetid: d9dcbdf0-ba35-4ebd-b6f2-f3c8bdfc0431
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a3d8b77833da20c4a0b4254d4ce3432ff20d2f9b18a1da877adc9664bbff6c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726061"
---
# <a name="enabled-property-command-object"></a>Proprietà Enabled (oggetto Command)

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta un **valore che indica** se il comando è abilitato nel menu a comparsa del carattere specificato.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agent***. Caratteri ("**_CharacterID_*_"). Commands("_*_name_*_"). Valore_ *  \[  =  *booleano abilitato*\]



| Parte      | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Espressione booleana che specifica se il **comando è** abilitato.<br/> <dl> <dt><span id="True"></span><span id="true"></span><span id="TRUE"></span>**Vero**</dt> <dd> Il **comando** è abilitato.<br/> </dd> <dt><span id="False"></span><span id="false"></span><span id="FALSE"></span>**Falso**</dt> <dd> Il **comando** è disabilitato.<br/> </dd> </dl> |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Se la [**proprietà Enabled**](enabled-property.md) è impostata su **True,** la didascalia degli oggetti [**Command**](/windows/desktop/lwef/the-command-object) viene visualizzata come testo normale nel menu a comparsa del carattere quando l'applicazione client è attiva per l'input. Se la **proprietà Enabled** è **False**, la didascalia viene visualizzata come testo non disponibile (disabilitato). Un comando **disabilitato** non è accessibile anche per l'input vocale.

 

