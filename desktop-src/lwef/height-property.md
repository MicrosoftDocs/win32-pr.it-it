---
title: Proprietà Height (oggetto characters)
description: Height (proprietà)
ms.assetid: 2c8dc333-e3c1-4f25-833b-9a4262c75b9f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e504dcbbfd470c62b4102d86f25a1d2b3c4c25e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739322"
---
# <a name="height-property-characters-object"></a>Proprietà Height (oggetto characters)

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta l'altezza del frame del carattere specificato.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agente ***. Caratteri ("**_CharacterID_*_")._ *  \[ =  *Valore* altezza\]



| Parte    | Descrizione                                                 |
|---------|-------------------------------------------------------------|
| *value* | Valore long integer che specifica l'altezza del frame del carattere. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

La proprietà **Height** è sempre espressa in pixel, rispetto alle coordinate dello schermo (in alto a sinistra). L'impostazione di questa proprietà si applica a tutti i client del carattere.

Anche se il carattere viene visualizzato in una finestra dell'area a forma irregolare, l'altezza del carattere è basata sulle dimensioni esterne del frame di animazione rettangolare usato quando il carattere è stato compilato con l'editor dei caratteri di Microsoft Agent.

 

 




