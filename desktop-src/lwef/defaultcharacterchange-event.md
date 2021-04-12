---
title: Evento DefaultCharacterChange
description: Evento DefaultCharacterChange
ms.assetid: 14b86a44-8fd2-4719-b7b5-cdcc618d27cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab92fe04f9c42466d559e9b4610eafc8490556d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396371"
---
# <a name="defaultcharacterchange-event"></a>Evento DefaultCharacterChange

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Si verifica quando l'utente modifica il carattere predefinito.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

**Sub** *Agent. * * * DefaultCharacterChange* *  **(ByVal** *GUID * * *)**



| Parte   | Descrizione                                      |
|--------|--------------------------------------------------|
| *GUID* | Restituisce l'identificatore univoco per il carattere. |



 

</dd> </dl>

### <a name="remarks"></a>Commenti

Questo evento indica quando l'utente ha modificato il carattere assegnato come carattere predefinito dell'utente. Il server invia questo solo ai client che hanno caricato il carattere predefinito.

Quando viene visualizzato il nuovo carattere, assume le stesse dimensioni di qualsiasi istanza già caricata del carattere o del carattere predefinito precedente (in quell'ordine).

### <a name="see-also"></a>Vedere anche

[**Metodo ShowDefaultCharacterProperties**](showdefaultcharacterproperties-method.md), [ **metodo Load**](load-method.md)


 

 




