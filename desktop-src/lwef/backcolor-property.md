---
title: Proprietà BackColor (funzionalità dell'ambiente Windows legacy)
description: BackColor (proprietà)
ms.assetid: a82c23bc-b280-4a52-9272-68879557cac7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3332fcc6a9081b52300dbee4c69c77602e84a62e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739655"
---
# <a name="backcolor-property-legacy-windows-environment-features"></a>Proprietà BackColor (funzionalità dell'ambiente Windows legacy)

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce il colore di sfondo attualmente visualizzato nella finestra del fumetto di Word per il carattere specificato.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agente ***. Caratteri ("**_CharacterID_*_"). Balloon. BackColor_*

</dd> </dl>

## <a name="remarks"></a>Commenti

L'intervallo valido per un colore RGB normale è compreso tra 0 e 16.777.215 (&HFFFFFF). L'alto byte di un numero in questo intervallo è uguale a 0; i 3 byte inferiori, dal meno significativo al più significativo, determinano rispettivamente la quantità di rosso, verde e blu. Ognuno dei componenti rosso, verde e blu è rappresentato da un numero compreso tra 0 e 255 (&HFF).

 

 




