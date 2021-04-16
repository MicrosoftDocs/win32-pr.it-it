---
description: Rich Edit 3,0 supporta l'IME HexToUnicode, che consente a un utente di eseguire la conversione tra caratteri esadecimali e Unicode usando i tasti di scelta rapida in uno dei due modi.
ms.assetid: 4b8c4de4-9c1c-459c-a640-367e86a9b9cc
title: IME HexToUnicode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88042ce276082755613b28a7e4d070c8b3d695f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530313"
---
# <a name="hextounicode-ime"></a>IME HexToUnicode

Rich Edit 3,0 supporta l'IME HexToUnicode, che consente a un utente di eseguire la conversione tra caratteri esadecimali e Unicode usando i tasti di scelta rapida in uno dei due modi.

Utilizzando il primo metodo di conversione, l'utente digita il codice carattere in formato esadecimale e quindi immette ALT + X. L'IME sostituisce le cifre esadecimali che precedono il punto di inserimento con il carattere Unicode. Se il tipo di carattere corrente non supporta il codice carattere, viene scelto un tipo di carattere appropriato che lo supporta. Per eseguire la conversione da Unicode ad esadecimale, l'utente immette MAIUSC + ALT + X. Questa voce sostituisce il carattere Unicode che precede il punto di inserimento con le cifre esadecimali. In particolare, questo metodo consente all'utente di determinare il carattere indicato da un indicatore "glifo mancante". Se il codice carattere esadecimale segue immediatamente alcuni caratteri esadecimali (non carattere) legittimi, l'utente seleziona le cifre specifiche da convertire prima di digitare ALT + X. Un problema con questo primo metodo è che ALT + X viene talvolta usato come combinazione di tasti per il comando Exit (ovvero eXit). Ad esempio, in Microsoft Office, questo comando viene visualizzato solo come opzione del menu **file** .

Il secondo metodo di conversione tra caratteri esadecimali e Unicode riguarda il tastierino numerico. Utilizzando questo metodo, l'utente digita ALT + numeri del tastierino numerico (con valori maggiori di 255) per immettere i caratteri Unicode utilizzando valori decimali. Questo metodo non è utile come il primo perché l'utente non è in grado di visualizzare le cifre esadecimali digitate. Inoltre, l'utente non è in grado di correggere le cifre esadecimali, ad eccezione di immettere nuovamente tutte le cifre.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su Gestione metodi di input](about-input-method-manager.md)
</dt> </dl>

 

 



