---
title: Metodo Show
description: Metodo Show
ms.assetid: 58adbb55-f4cb-4356-abc4-b85fa3af744d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ede9dd8474b21911fccb0c217b070dbfb84160125d2fd56092685ccaf82905b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118475353"
---
# <a name="show-method"></a>Metodo Show

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Rende visibile il carattere specificato e riproduce l'animazione **Showing** associata.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agent***. Caratteri ("**_CharacterID_*_"). Mostra_ *  \[ *veloce*\]



| Parte   | Descrizione                                                                                                                                                                                                                              |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Veloce* | facoltativo. Espressione booleana che specifica se il server riproduce **l'animazione Showing.** **True** Ignora **l'animazione Showing** state (Visualizzazione dello stato). <br/> **False** (impostazione predefinita) Non ignora l'animazione **Showing** state (Visualizzazione dello stato). <br/> |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Se si dichiara un riferimento a un oggetto e lo si imposta su questo metodo, viene restituito un [**oggetto Request.**](/windows/desktop/lwef/the-request-object) Inoltre, se l'animazione **Showing** associata non è stata caricata e il  parametro **Fast** non è stato specificato **come True,** il server imposta la proprietà Status dell'oggetto [**Request**](status-property.md) su "failed" con un numero di errore appropriato. Pertanto, se si usa il protocollo HTTP per accedere ai dati di animazione dei caratteri, usare il metodo [**Get**](get-method.md) per caricare l'animazione **dello** stato Showing prima di chiamare il **metodo Show.**

Evitare di impostare **il parametro Fast** su True **senza** prima riprodurre un'animazione; In caso contrario, il frame di caratteri potrebbe essere visualizzato senza immagine. In particolare, si noti che se si chiama [**MoveTo**](moveto-method.md) quando il carattere non è visibile, non viene riprodotta alcuna animazione. Pertanto, se si chiama il **metodo Show** con **Fast** impostato su **True,** non verrà visualizzata alcuna immagine. Analogamente, se si chiama [**Nascondi e**](hide-method.md) mostra **con** **Fast** impostato su **True,** non sarà presente alcuna immagine visibile.

## <a name="see-also"></a>Vedere anche

[**Hide (metodo)**](hide-method.md)


 

