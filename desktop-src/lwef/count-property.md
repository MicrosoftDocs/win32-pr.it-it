---
title: Proprietà Count
description: Proprietà Count
ms.assetid: a0375aa9-495d-47be-a3f7-4d5987688555
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 630817a8370a071851216ab03d43493e672b3e0a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872394"
---
# <a name="count-property"></a>Proprietà Count

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce un valore Long Integer (proprietà di sola lettura) che specifica il numero di oggetti [**Command**](/windows/desktop/lwef/the-command-object) nella raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) .

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agente ***. Caratteri ("*** CharacterID * * *"). Commands. Count**

</dd> </dl>

## <a name="remarks"></a>Commenti

Il **conteggio** include solo il numero di oggetti [**Command**](/windows/desktop/lwef/the-command-object) definiti nella raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) . Il server o altre voci client non sono incluse.

 

 