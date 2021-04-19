---
description: Un terminale multitraccia può essere considerato come un terminale che è una raccolta di altri terminali. Ogni terminale figlio (a &\# 0034; track&\# 0034;) può essere un terminale multitraccia o un terminale a traccia singola.
ms.assetid: bf23bc26-5763-45a3-a63d-e43ce2480956
title: Informazioni sui terminali multitraccia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58042236c737f6ab0b933699d75e19358f6e6b81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311914"
---
# <a name="about-multitrack-terminals"></a>Informazioni sui terminali multitraccia

Un terminale multitraccia può essere considerato come un terminale che è una raccolta di altri terminali. Ogni terminale figlio ("Track") può essere un terminale multitraccia o un terminale a singolo rilevamento.

Tutti i terminali Multitrack espongono l'interfaccia [**ITMultiTrackTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) , che include metodi generici per l'enumerazione, la creazione e la rimozione di terminali di rilevamento da un terminale multitraccia. Tutti i terminali, a traccia singola e multitraccia, espongono l'interfaccia [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) .

Un client che dispone di un puntatore a un'interfaccia [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) può individuare se il terminale è multitraccia o a traccia singola eseguendo una query sul terminale per l'interfaccia [**ITMultiTrackTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) , che viene esposta solo nei terminali Multitrack.

Il terminale padre può usare l'interfaccia [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) dei terminali di tracking oppure potrebbe essere necessario tenere traccia dei terminali per esporre le interfacce private.

Per altre informazioni, vedere [tenere traccia dei terminali](track-terminals.md).

 

 
