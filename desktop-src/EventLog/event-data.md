---
description: A ogni evento possono essere associati dati specifici degli eventi.
ms.assetid: fa2f9e71-44c3-4569-bde4-24112a756664
title: Dati eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 459377d9cdf78fba46133b494723008df025caad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308373"
---
# <a name="event-data"></a>Dati eventi

A ogni evento possono essere associati dati specifici degli eventi. Il Visualizzatore eventi non interpreta questi dati. vengono visualizzati dati aggiuntivi solo in un formato esadecimale e di testo combinato. Il limite massimo per la dimensione di un evento nel log even è 0x3FFFF bytes. Pertanto, utilizzare dati specifici degli eventi sporadicamente, inclusi solo se si è certi che saranno utili a un utente che esegue il debug di un problema. Molti eventi correlati alla rete, ad esempio, includono i blocchi di controllo di rete (BCN) come dati specifici degli eventi.

Quando si usano dati specifici degli eventi, l'ultima parte della relativa stringa di descrizione deve fornire una nota sulle informazioni fornite come dati specifici dell'evento. Il software di rete, ad esempio, potrebbe fornire una nota come: "(la BCN è costituita dai dati dell'evento)". Come convenzione, usare le parentesi per racchiudere tali osservazioni, come indicato in questo esempio.

È anche possibile usare dati specifici dell'evento per archiviare le informazioni che l'applicazione può elaborare in modo indipendente dal Visualizzatore eventi. Ad esempio, è possibile scrivere un visualizzatore specifico per gli eventi oppure scrivere un programma che analizza il log e crea un report che include le informazioni dei dati specifici dell'evento.

 

 



