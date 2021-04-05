---
title: Tag MRK
description: Tag MRK
ms.assetid: 1bc04853-f919-4f6f-90c2-21ac836bb1e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 805a66b9ce5863bda7b7b95317bcab9cf1d80f32
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710510"
---
# <a name="mrk-tag"></a>Tag MRK

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Definisce un segnalibro nel testo parlato.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

**\\MRK =***numero***\\**



| Parte     | Descrizione                                        |
|----------|----------------------------------------------------|
| *number* | Valore long integer che identifica il segnalibro. |



 

</dd> </dl>

### <a name="remarks"></a>Commenti

Quando il server elabora un segnalibro, genera un evento di segnalibro. È necessario specificare un numero maggiore di zero (0) e non uguale a 2147483647 o 2147483646.

 

 




