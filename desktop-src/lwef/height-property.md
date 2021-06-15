---
title: Proprietà Height (oggetto Characters)
description: Informazioni sulla proprietà Height dell'oggetto Characters. Microsoft Agent è deprecato a livello di Windows 7.
ms.assetid: 2c8dc333-e3c1-4f25-833b-9a4262c75b9f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d93d288276bd9717378c9a1ab0d9b00489959c00
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068512"
---
# <a name="height-property-characters-object"></a>Proprietà Height (oggetto Characters)

\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta l'altezza del frame del carattere specificato.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agent***. Caratteri ("**_CharacterID_*_"). Valore_ *  \[ =  *altezza*\]



| Parte    | Descrizione                                                 |
|---------|-------------------------------------------------------------|
| *value* | Valore Long Integer che specifica l'altezza del frame del carattere. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

La **proprietà Height** è sempre espressa in pixel, rispetto alle coordinate dello schermo (in alto a sinistra). L'impostazione di questa proprietà si applica a tutti i client del carattere.

Anche se il carattere viene visualizzato in una finestra di area di forma irregolare, l'altezza del carattere si basa sulle dimensioni esterne del frame di animazione rettangolare usato quando il carattere è stato compilato con l'editor di caratteri di Microsoft Agent.

 

 




