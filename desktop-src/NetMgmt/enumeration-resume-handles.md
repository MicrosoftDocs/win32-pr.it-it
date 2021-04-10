---
title: Handle di ripresa dell'enumerazione
description: Gli handle di ripresa dell'enumerazione sono identificatori per la chiave di ripresa effettiva contenuta nei dati dell'istanza per la funzione. Questa operazione è necessaria per la sicurezza, l'interoperabilità e per semplificare il codice chiamante per la funzione.
ms.assetid: 6734e99b-7f8c-43c9-96e3-44c9783960dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61f20e7a7d5e1f9afb15e6adad4c0d7643bf841d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955499"
---
# <a name="enumeration-resume-handles"></a>Handle di ripresa dell'enumerazione

Gli handle di ripresa dell'enumerazione sono identificatori per la chiave di ripresa effettiva contenuta nei dati dell'istanza per la funzione. Questa operazione è necessaria per la sicurezza, l'interoperabilità e per semplificare il codice chiamante per la funzione.

Se viene passato un **valore null** per il puntatore al punto di ripristino, non viene archiviato alcun handle e non è possibile continuare la ricerca dell'enumerazione. Questa operazione è utile nei casi in cui l'applicazione non desidera enumerare tutti gli elementi.

Se viene restituito un errore da una chiamata di enumerazione, l'handle di ripresa deve essere considerato non valido e non usato per le successive chiamate di enumerazione. Quando si verifica questa situazione, è necessario riavviare l'enumerazione dall'inizio.

 

 




