---
title: Evento segnalibro
description: Evento segnalibro
ms.assetid: 6733cd4e-2ba0-4cff-b68d-abfea284f748
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0695ccd04f93eae46eaae66955c84fefb9e0c963
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221268"
---
# <a name="bookmark-event"></a>Evento segnalibro

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Si verifica quando viene attivato un segnalibro in una stringa di testo vocale definita dall'applicazione.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

  \_ **Segnalibro** Sub Agent **(ByVal** *BookmarkID * * *)**



| Parte         | Descrizione                                     |
|--------------|-------------------------------------------------|
| *BookmarkID* | Valore long integer che identifica il numero di segnalibri. |



 

</dd> </dl>

### <a name="remarks"></a>Commenti

Per specificare un evento di segnalibro, usare il metodo [**Speak**](speak-method.md) con un tag **MRK** nel testo fornito. Per altre informazioni sui tag, vedere Tag di output vocale.

 

 




