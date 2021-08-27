---
description: Descrizione dei conflitti tra movimenti dell'applicazione e caratteri e simboli.
ms.assetid: c9b8c284-7c31-4fb0-8cc4-ff09c9c4f228
title: Conflitti tra movimenti e caratteri e simboli dell'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5819bfd7013bc39ecb622b09a1ae42816bb969ec63bf062d19597575bb958279
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009021"
---
# <a name="conflicts-between-application-gestures-and-characters-and-symbols"></a>Conflitti tra movimenti e caratteri e simboli dell'applicazione

Alcuni movimenti dell'applicazione possono essere in conflitto con caratteri, combinazioni di caratteri, simboli, combinazioni di caratteri e simboli o parole intere scritte in un singolo tratto. La maggior parte di questi conflitti viene evitata con una conoscenza dettagliata del contesto in cui viene eseguito il movimento dell'applicazione.

Ad esempio, per distinguere un movimento a destra da un trattino (-) o un carattere di sottolineatura ( ), un'applicazione può filtrare la vicinanza del movimento ai caratteri adiacenti, la dimensione relativa rispetto ai caratteri o altre informazioni contenute in un \_ pacchetto. La tempistica del movimento dell'applicazione può anche essere un fattore determinante nella scelta tra movimenti e caratteri. Prima di applicare un movimento dell'applicazione potrebbe essere presente più una pausa rispetto all'immissione di caratteri. A meno che un utente non esezioni una serie di movimenti di annullamento o backspace, potrebbe anche essere presente più di una pausa dopo un movimento che di un carattere.

Gli argomenti seguenti descrivono in dettaglio questi conflitti:

-   [Conflitti con caratteri latini e simboli](conflicts-with-latin-characters-and-symbols.md)
-   [Conflitti con East-Asian caratteri](conflicts-with-east-asian-characters.md)

 

 



