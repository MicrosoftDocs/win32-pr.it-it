---
title: Evento Bookmark
description: Evento Bookmark
ms.assetid: 6733cd4e-2ba0-4cff-b68d-abfea284f748
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c6a6dcd072b87c6a924c8d33e6ebb73c75c927bdf955f51612703d3fc18af79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976711"
---
# <a name="bookmark-event"></a>Evento Bookmark

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Si verifica quando viene attivato un segnalibro in una stringa di testo vocale definito dall'applicazione.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

**Sub** *agent* \_ **Bookmark** **(ByVal** *BookmarkID***)**



| Parte         | Descrizione                                     |
|--------------|-------------------------------------------------|
| *BookmarkID* | Valore Long Integer che identifica il numero del segnalibro. |



 

</dd> </dl>

### <a name="remarks"></a>Commenti

Per specificare un evento segnalibro, usare [**il metodo Speak**](speak-method.md) con un tag **Mrk** nel testo fornito. Per altre informazioni sui tag, vedere Tag di output vocale.

 

 




