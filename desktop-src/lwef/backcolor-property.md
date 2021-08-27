---
title: Proprietà BackColor (funzionalità dell'Windows legacy)
description: Proprietà BackColor
ms.assetid: a82c23bc-b280-4a52-9272-68879557cac7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f799e8b9e00a97770cd004e29df75da8345a6cc01531fce53079ea550402c68d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114811"
---
# <a name="backcolor-property-legacy-windows-environment-features"></a>Proprietà BackColor (funzionalità dell'Windows legacy)

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce il colore di sfondo attualmente visualizzato nella finestra del fumetto per il carattere specificato.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agent***. Caratteri ("**_CharacterID_*_"). Balloon.BackColor_*

</dd> </dl>

## <a name="remarks"></a>Commenti

L'intervallo valido per un colore RGB normale è compreso tra 0 e 16.777.215 (&HFFFFFF). Il byte più alto di un numero in questo intervallo è uguale a 0; i 3 byte inferiori, dal byte meno significativo al più significativo, determinano rispettivamente la quantità di rosso, verde e blu. Ognuno dei componenti rosso, verde e blu è rappresentato da un numero compreso tra 0 e 255 (&HFF).

 

 




