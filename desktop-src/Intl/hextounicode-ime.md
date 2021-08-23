---
description: Rich Edit 3.0 supporta l'IME HexToUnicode, che consente a un utente di eseguire la conversione tra caratteri esadecimali e Unicode usando i tasti di scelta rapida in due modi.
ms.assetid: 4b8c4de4-9c1c-459c-a640-367e86a9b9cc
title: HexToUnicode IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5a57ce56821f200c9fd9ff80560908f5a72ecfdb0f51ce981e1aff40ce785b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068151"
---
# <a name="hextounicode-ime"></a>HexToUnicode IME

Rich Edit 3.0 supporta l'IME HexToUnicode, che consente a un utente di eseguire la conversione tra caratteri esadecimali e Unicode usando i tasti di scelta rapida in due modi.

Usando il primo metodo di conversione, l'utente digita il codice carattere in formato esadecimale e quindi immette ALT+X. L'IME sostituisce le cifre esadecimali che precedono il punto di inserimento con il carattere Unicode. Se il tipo di carattere corrente non supporta il codice carattere, viene scelto un tipo di carattere appropriato che lo supporta. Per eseguire la conversione da Unicode a esadecimale, l'utente immette MAIUSC+ALT+X. Questa voce sostituisce il carattere Unicode che precede il punto di inserimento con le cifre esadecimali. In particolare, questo metodo consente all'utente di determinare il carattere indicato da un indicatore "glifo mancante". Se il codice carattere esadecimale segue immediatamente alcuni caratteri esadecimali legittimi (non carattere), l'utente seleziona le cifre specifiche da convertire prima di digitare ALT+X. Un problema con questo primo metodo è che ALT+X viene talvolta usato come combinazione di tasti per il comando exit ,ovvero eXit. Ad esempio, in Microsoft Office, questo comando viene visualizzato solo come opzione del menu **File.**

Il secondo metodo di conversione tra caratteri esadecimali e Unicode prevede il tastierino numerico. Usando questo metodo, l'utente digita i numeri ALT+NumPad (con valori maggiori di 255) per immettere caratteri Unicode usando valori decimali. Questo metodo non è utile come il primo perché l'utente non può vedere quali cifre esadecimali sono state digitate. Inoltre, l'utente non può correggere le cifre esadecimali se non immettendo nuovamente tutte le cifre.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su Gestione metodi di input](about-input-method-manager.md)
</dt> </dl>

 

 



