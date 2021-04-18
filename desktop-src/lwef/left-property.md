---
title: Proprietà Left (oggetto characters)
description: Left (proprietà)
ms.assetid: f496f075-6430-4806-a237-1c7b626d355e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a318e659405883c56f296a9371eba7e9423662b1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300911"
---
# <a name="left-property-characters-object"></a>Proprietà Left (oggetto characters)

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta il bordo sinistro del frame del carattere specificato.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agente ***. Caratteri ("**_CharacterID_*_")._ *  \[  =  *Valore* a sinistra\]



| Parte    | Descrizione                                                           |
|---------|-----------------------------------------------------------------------|
| *value* | Valore long integer che specifica il bordo sinistro del frame del carattere. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

La proprietà **Left** è sempre espressa in pixel, in relazione all'origine dello schermo (in alto a sinistra). L'impostazione di questa proprietà si applica a tutti i client del carattere.

Anche se il carattere viene visualizzato in una finestra dell'area a forma irregolare, la posizione del carattere è basata sulle dimensioni esterne del frame di animazione rettangolare usato quando il carattere è stato compilato con l'editor dei caratteri di Microsoft Agent.

 

 




