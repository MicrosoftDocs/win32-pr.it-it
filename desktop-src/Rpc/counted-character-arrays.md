---
title: Matrici di caratteri conteggiati
description: L'attributo \ size is\ indica il limite superiore della matrice, mentre l'attributo \ length is\ indica il numero di elementi della matrice \_ \_ da trasmettere.
ms.assetid: bed10259-3034-4be8-91f5-5201c2e19c6b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea8abb7a391c617cadae5af396c4b4216dc9d14abf0f6d31ead3a6e075c7357b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118931130"
---
# <a name="counted-character-arrays"></a>Matrici di caratteri conteggiati

\[ [ \_ L'attributo size](/windows/desktop/Midl/size-is) indica il limite superiore della \] matrice, mentre length \[ [ \_ è](/windows/desktop/Midl/length-is) attribute indica il numero di elementi della matrice \] da trasmettere. Oltre alla matrice , il prototipo di procedura remota deve includere tutte le variabili che rappresentano la lunghezza o le dimensioni che determinano gli elementi della matrice trasmessi (possono essere parametri separati o aggregati con la stringa in una struttura ). Questi attributi possono essere usati con matrici di caratteri wide o a byte singolo esattamente come con matrici di altri tipi.

Le informazioni contenute in questa sezione descrivono i prototipi dei parametri di procedura remota per le matrici di caratteri. È suddiviso negli argomenti seguenti:

-   [\[in, out, size \_ è \] Prototype](-in-out-size-is-prototype.md)
-   [\[in, size \_ is and out, size \_ is \] Prototype](-in-size-is-and-out-size-is-prototype.md)

 

 