---
title: Proprietà Left (oggetto Characters)
description: Informazioni sulla proprietà dell'oggetto Left Characters. Microsoft Agent è deprecato a livello di Windows 7.
ms.assetid: f496f075-6430-4806-a237-1c7b626d355e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e2f860e6827a9c96c42014456e43b791ab70ed4
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/10/2021
ms.locfileid: "111988937"
---
# <a name="left-property-characters-object"></a>Proprietà Left (oggetto Characters)

\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta il bordo sinistro della cornice del carattere specificato.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agent***. Caratteri ("**_CharacterID_*_"). Valore_ *  \[  =  *a sinistra*\]



| Parte    | Descrizione                                                           |
|---------|-----------------------------------------------------------------------|
| *value* | Valore Long integer che specifica il bordo sinistro della cornice del carattere. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

La **proprietà Left** è sempre espressa in pixel, rispetto all'origine dello schermo (in alto a sinistra). L'impostazione di questa proprietà si applica a tutti i client del carattere.

Anche se il carattere viene visualizzato in una finestra di area irregolare, la posizione del carattere è basata sulle dimensioni esterne del frame di animazione rettangolare usato quando il carattere è stato compilato con Microsoft Agent Character Editor.

 

 




