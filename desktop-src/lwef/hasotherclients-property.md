---
title: Proprietà HasOtherClients
description: Proprietà HasOtherClients
ms.assetid: 5ecc6f42-786b-40a6-8800-9ad0d92edfb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc3434cec191d2bec93d501847df064a8dbbf3e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044744"
---
# <a name="hasotherclients-property"></a>Proprietà HasOtherClients

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce un valore che indica se il carattere specificato è utilizzato da altre applicazioni.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agente*. **Caratteri ("***CharacterID***"). HasOtherClients**



| Valore     | Descrizione                                |
|-----------|--------------------------------------------|
| **True**  | Il carattere dispone di altri client.           |
| **False** | Il carattere non dispone di altri client. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

È possibile usare questa proprietà per determinare se l'applicazione è l'unico o l'ultimo client del carattere, quando più di un'applicazione condivide (ha caricato) lo stesso carattere.

 

 




