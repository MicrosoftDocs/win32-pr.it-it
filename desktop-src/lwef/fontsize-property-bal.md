---
title: Proprietà FontSize (oggetto Balloon)
description: Informazioni sulla proprietà dell'oggetto FontSize Balloon. Microsoft Agent è deprecato a livello di Windows 7.
ms.assetid: 36d5526a-1ae9-4ef2-94f6-0ad63ce86882
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85e6a2c13708d3066faaf396a3a451c9be01d177
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068218"
---
# <a name="fontsize-property-balloon-object"></a>Proprietà FontSize (oggetto Balloon)

\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta la dimensione del carattere supportata per il fumetto per il carattere specificato.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agent.***Caratteri* *  **("**_CharacterID_*_"). Balloon.FontSize_* \[  =  *Points*\]



| Parte     | Descrizione                                              |
|----------|----------------------------------------------------------|
| *Punti* | Valore Long Integer che specifica la dimensione del carattere in punti. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

La [**proprietà FontSize**](fontsize-property.md) restituisce un valore Long Integer che specifica le dimensioni correnti del carattere in punti. Il valore massimo per **FontSize** è 2160 punti.

Il valore predefinito per le impostazioni del carattere del fumetto di un carattere viene impostato nell'Editor caratteri di Microsoft Agent. Inoltre, l'utente può eseguire l'override delle impostazioni dei caratteri per tutti i caratteri nella finestra delle proprietà di Microsoft Agent.

 

 




