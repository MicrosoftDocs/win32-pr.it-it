---
title: Metodo Unload
description: Metodo Unload
ms.assetid: 2ffaeea6-ff24-48b2-bc99-eba429434a30
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41d19f5f29647ff01b5a52bd8978694aaef1c43a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725914"
---
# <a name="unload-method"></a>Metodo Unload

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Scarica i dati di tipo carattere per il carattere specificato.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agente ***. Caratteri. Unload "*** CharacterID * * *"**

</dd> </dl>

## <a name="remarks"></a>Commenti

Utilizzare questo metodo quando non è più necessario un carattere, per liberare memoria utilizzata per archiviare le informazioni sul carattere. Se si accede di nuovo al carattere, utilizzare il metodo [**Load**](load-method.md) .

Questo metodo non restituisce un oggetto [**Request**](/windows/desktop/lwef/the-request-object) .

 

 