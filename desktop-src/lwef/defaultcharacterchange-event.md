---
title: Evento DefaultCharacterChange
description: Evento DefaultCharacterChange
ms.assetid: 14b86a44-8fd2-4719-b7b5-cdcc618d27cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eed166608d3f3b874e975ff58f600d24b73b50e293333b841039b2240780b4de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963131"
---
# <a name="defaultcharacterchange-event"></a>Evento DefaultCharacterChange

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Si verifica quando l'utente modifica il carattere predefinito.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

**Sub** *agent.***DefaultCharacterChange* *  **(ByVal** *GUID***)**



| Parte   | Descrizione                                      |
|--------|--------------------------------------------------|
| *GUID* | Restituisce l'identificatore univoco per il carattere. |



 

</dd> </dl>

### <a name="remarks"></a>Commenti

Questo evento indica quando l'utente ha modificato il carattere assegnato come carattere predefinito dell'utente. Il server lo invia solo ai client che hanno caricato il carattere predefinito.

Quando viene visualizzato il nuovo carattere, assume le stesse dimensioni di qualsiasi istanza già caricata del carattere o del carattere predefinito precedente (in questo ordine).

### <a name="see-also"></a>Vedere anche

[**Metodo ShowDefaultCharacterProperties**](showdefaultcharacterproperties-method.md), [ **metodo Load**](load-method.md)


 

 




