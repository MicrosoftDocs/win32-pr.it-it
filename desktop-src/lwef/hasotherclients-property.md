---
title: Proprietà HasOtherClients
description: Proprietà HasOtherClients
ms.assetid: 5ecc6f42-786b-40a6-8800-9ad0d92edfb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf7bb91240ade815c00fb2e36adf1466dcb30ba4240be038342906be49e6ff2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118479006"
---
# <a name="hasotherclients-property"></a>Proprietà HasOtherClients

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce un valore che indica se il carattere specificato è utilizzato da altre applicazioni.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*Agent*. **Characters("**_CharacterID_*_"). HasOtherClients_*



| Valore     | Descrizione                                |
|-----------|--------------------------------------------|
| **True**  | Il carattere ha altri client.           |
| **False** | Il carattere non ha altri client. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

È possibile usare questa proprietà per determinare se l'applicazione è l'unico o l'ultimo client del carattere, quando più di un'applicazione condivide (ha caricato) lo stesso carattere.

 

 




