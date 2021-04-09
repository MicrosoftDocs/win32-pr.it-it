---
title: ForeColor (proprietà)
description: ForeColor (proprietà)
ms.assetid: b5cef81b-55e1-49a5-bdbf-f7101520a13a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ef05c9f51e040326c75f142e4649a8dbd0cfdbb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855633"
---
# <a name="forecolor-property"></a>ForeColor (proprietà)

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce il colore di primo piano attualmente visualizzato nella finestra del fumetto di Word per il carattere specificato.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agente ***. Caratteri ("*** CharacterID * * *"). Balloon. ForeColor**

</dd> </dl>

## <a name="remarks"></a>Commenti

La proprietà **ForeColor** restituisce un valore che specifica il colore del testo nel fumetto di Word. L'intervallo valido per un colore RGB normale è compreso tra 0 e 16.777.215 (&HFFFFFF). L'alto byte di un numero in questo intervallo è uguale a 0; i 3 byte inferiori, dal meno significativo al più significativo, determinano rispettivamente la quantità di rosso, verde e blu. Ognuno dei componenti rosso, verde e blu è rappresentato da un numero compreso tra 0 e 255 (&HFF).

 

 




