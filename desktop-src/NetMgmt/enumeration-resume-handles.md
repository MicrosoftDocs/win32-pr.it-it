---
title: Handle di ripresa dell'enumerazione
description: Gli handle di ripresa dell'enumerazione sono identificatori per la chiave di ripresa effettiva contenuta nei dati dell'istanza per la funzione. Questa operazione è necessaria per la sicurezza, l'interoperabilità e per semplificare il codice chiamante per la funzione.
ms.assetid: 6734e99b-7f8c-43c9-96e3-44c9783960dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10976661723af59af945b9dec1080196e682b308fa1a597edfc4cee6047aa783
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912191"
---
# <a name="enumeration-resume-handles"></a>Handle di ripresa dell'enumerazione

Gli handle di ripresa dell'enumerazione sono identificatori per la chiave di ripresa effettiva contenuta nei dati dell'istanza per la funzione. Questa operazione è necessaria per la sicurezza, l'interoperabilità e per semplificare il codice chiamante per la funzione.

Se viene **passato un valore NULL** per il puntatore all'handle di ripresa, non viene archiviato alcun handle e non è possibile continuare la ricerca di enumerazione. Ciò è utile nei casi in cui l'applicazione non desidera enumerare tutti gli elementi.

Se viene restituito un errore da una chiamata di enumerazione, l'handle di ripresa deve essere considerato non valido e non utilizzato per le chiamate di enumerazione successive. In questo caso è necessario riavviare l'enumerazione dall'inizio.

 

 




