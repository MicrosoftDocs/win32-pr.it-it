---
description: Descrizione dei conflitti tra i movimenti dell'applicazione e i caratteri e i simboli.
ms.assetid: c9b8c284-7c31-4fb0-8cc4-ff09c9c4f228
title: Conflitti tra movimenti dell'applicazione e caratteri e simboli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a92755990235d494cd3e0dc07218de8a1e47d578
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305685"
---
# <a name="conflicts-between-application-gestures-and-characters-and-symbols"></a>Conflitti tra movimenti dell'applicazione e caratteri e simboli

Alcuni movimenti dell'applicazione possono entrare in conflitto con caratteri, combinazioni di caratteri, simboli, combinazioni di caratteri e simboli o parole intere scritte in un singolo tratto. La maggior parte di questi conflitti viene evitata con una conoscenza approfondita del contesto in cui viene eseguito il movimento dell'applicazione.

Ad esempio, per distinguere un gesto destro da un trattino (-) o da un carattere di sottolineatura ( \_ ), un'applicazione può filtrare in base al modo in cui il movimento si avvicina ai caratteri adiacenti, alla dimensione relativa rispetto ai caratteri o ad altre informazioni contenute in un pacchetto. La tempistica del movimento dell'applicazione può anche essere un fattore determinante nella scelta tra movimenti e caratteri. Prima di applicare un movimento di un'applicazione, è possibile che si verifichi una pausa prima di inserire i caratteri. A meno che un utente non esegua una serie di movimenti di annullamento o BACKSPACE, potrebbe anche esserci più di una pausa dopo un movimento rispetto a un carattere.

Gli argomenti seguenti illustrano in dettaglio questi conflitti:

-   [Conflitti con caratteri latini e simboli](conflicts-with-latin-characters-and-symbols.md)
-   [Conflitti con caratteri East-Asian](conflicts-with-east-asian-characters.md)

 

 



