---
title: Mostra metodo
description: Mostra metodo
ms.assetid: 58adbb55-f4cb-4356-abc4-b85fa3af744d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a05a1adaa46c85f34e02128960330c68d9a86db1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299595"
---
# <a name="show-method"></a>Mostra metodo

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Rende visibile il carattere specificato e riproduce l'animazione di **visualizzazione** associata.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agente ***. Caratteri ("*** CharacterID * * *"). Mostra* *  \[ *veloce*\]



| Parte   | Descrizione                                                                                                                                                                                                                              |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Veloce* | facoltativo. Espressione booleana che specifica se il server riproduce l'animazione di **visualizzazione** . Valore **true** Ignora l'animazione dello stato di **visualizzazione** . <br/> **False** (impostazione predefinita) non ignora l'animazione dello stato di **visualizzazione** . <br/> |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Se si dichiara un riferimento a un oggetto e lo si imposta su questo metodo, viene restituito un oggetto [**Request**](/windows/desktop/lwef/the-request-object) . Inoltre, se non è stata caricata la **visualizzazione** dell'animazione associata e il parametro **Fast** non è stato specificato come **true**, il server imposta la proprietà [**status**](status-property.md) dell'oggetto **richiesta** su "failed" con un numero di errore appropriato. Se pertanto si utilizza il protocollo HTTP per accedere ai dati di animazione dei caratteri, utilizzare il metodo [**Get**](get-method.md) per caricare l'animazione **di visualizzazione dello stato prima** di chiamare il metodo **show** .

Evitare di impostare il parametro **Fast** su **true** senza prima riprodurre prima un'animazione. in caso contrario, il frame di caratteri può essere visualizzato senza immagine. In particolare, si noti che se si chiama [**MoveTo**](moveto-method.md) quando il carattere non è visibile, non viene eseguita alcuna animazione. Se pertanto si chiama il metodo **show** con **Fast** impostato su **true**, non viene visualizzata alcuna immagine. Analogamente, se si chiama [**Nascondi**](hide-method.md) e **Mostra** con **Fast** impostato su **true**, non sarà presente alcuna immagine visibile.

## <a name="see-also"></a>Vedere anche

[**Hide (metodo)**](hide-method.md)


 

