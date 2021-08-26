---
title: Proprietà ForeColor
description: Proprietà ForeColor
ms.assetid: b5cef81b-55e1-49a5-bdbf-f7101520a13a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cebfc7f0b64a43f7ccb9075426a75df9a777fbb8b1e5e94cb16e747e0681cb4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962761"
---
# <a name="forecolor-property"></a>Proprietà ForeColor

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce il colore di primo piano attualmente visualizzato nella finestra del fumetto per il carattere specificato.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agent***. Caratteri ("**_CharacterID_*_"). Balloon.ForeColor_*

</dd> </dl>

## <a name="remarks"></a>Commenti

La **proprietà ForeColor** restituisce un valore che specifica il colore del testo nel fumetto. L'intervallo valido per un colore RGB normale è compreso tra 0 e 16.777.215 (&HFFFFFF). Il byte alto di un numero in questo intervallo è uguale a 0. i 3 byte inferiori, dal byte meno significativo al byte più significativo, determinano rispettivamente la quantità di rosso, verde e blu. Ognuno dei componenti rosso, verde e blu è rappresentato da un numero compreso tra 0 e 255 (&HFF).

 

 




