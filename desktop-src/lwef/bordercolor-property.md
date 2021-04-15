---
title: BorderColor (proprietà)
description: BorderColor (proprietà)
ms.assetid: 7592db02-c157-45f4-bbcf-e6d5bd99e8e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6981d3ac280669f64219961b74d05c6ba73f1008
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471206"
---
# <a name="bordercolor-property"></a>BorderColor (proprietà)

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce il colore del bordo attualmente visualizzato per la finestra del fumetto di Word per il carattere specificato.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

* Agent ***. Caratteri ("*** CharacterID ***").** Balloon. BorderColor

</dd> </dl>

## <a name="remarks"></a>Commenti

L'intervallo valido per un colore RGB normale è compreso tra 0 e 16.777.215 (&HFFFFFF). L'alto byte di un numero in questo intervallo è uguale a 0; i 3 byte inferiori, dal meno significativo al più significativo, determinano rispettivamente la quantità di rosso, verde e blu. Ognuno dei componenti rosso, verde e blu è rappresentato da un numero compreso tra 0 e 255 (&HFF).

 

 




