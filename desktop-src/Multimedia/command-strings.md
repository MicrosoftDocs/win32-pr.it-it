---
title: Stringhe di comando
description: Stringhe di comando
ms.assetid: ca9ca153-f2bf-45ed-84e6-44e86e8efaed
keywords:
- Stringhe di comando MCI, informazioni
- Stringhe di comando MCI, sintassi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b62013abff091f668a3b045e9f3ca2e8745f0d9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398860"
---
# <a name="command-strings"></a>Stringhe di comando

Per inviare un comando stringa a un dispositivo MCI, usare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) , che include i parametri per il comando stringa e un buffer per tutte le informazioni restituite.

La funzione **mciSendString** restituisce zero in caso di esito positivo. Se la funzione ha esito negativo, la parola di ordine inferiore del valore restituito contiene un codice di errore. È possibile passare questo codice di errore alla funzione [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) per ottenere una descrizione di testo dell'errore.

## <a name="syntax-of-command-strings"></a>Sintassi delle stringhe di comando

Le stringhe di comando MCI usano una sintassi coerente di modificatore di oggetti verbo. Ogni stringa di comando include un comando, un identificatore di dispositivo e gli argomenti del comando. Gli argomenti sono facoltativi per alcuni comandi e sono obbligatori per altri.

Una stringa di comando ha il formato seguente:

*\_argomenti ID dispositivo comando*

Questi componenti contengono le informazioni seguenti:

-   Il *comando* specifica un comando MCI, ad esempio [**Open**](open.md), [**Close**](close.md)o [**Play**](play.md).
-   L' *\_ ID dispositivo* identifica un'istanza di un driver MCI. L' *\_ ID dispositivo* viene creato quando il dispositivo viene aperto.
-   Gli *argomenti* specificano i flag e le variabili utilizzati dal comando. I flag sono parole chiave riconosciute con il comando MCI. Le variabili sono numeri o stringhe che si applicano al comando o al flag MCI.

    Ad esempio, il comando **Play** usa gli argomenti "from *position* " e "to *position* " per indicare le posizioni in cui iniziare e terminare Play. È possibile elencare i flag utilizzati con un comando in qualsiasi ordine. Quando si usa un flag a cui è associata una variabile, è necessario specificare un valore per la variabile.

    Gli argomenti del comando non specificati (e facoltativi) presuppongono un valore predefinito.

La funzione di esempio seguente invia il comando [**Play**](play.md) con i flag "from" e "to".


```C++
BOOL PlayFromTo(LPTSTR lpstrAlias, DWORD dwFrom, DWORD dwTo) 
{ 
    TCHAR achCommandBuff[128]; 
    int result;
    MCIERROR err;

    // Form the command string.
    result = _stprintf_s(
        achCommandBuff, 
        TEXT("play %s from %u to %u"), 
        lpstrAlias, dwFrom, dwTo); 

    if (result == -1)
    {
        return FALSE;
    }

    // Send the command string.
    err = mciSendString(achCommandBuff, NULL, 0, NULL); 
    if (err != 0)
    {
        return FALSE;
    }

    return TRUE;
} 
```



## <a name="data-types-for-command-variables"></a>Tipi di dati per le variabili di comando

È possibile utilizzare i tipi di dati seguenti per le variabili in una stringa di comando.



| **Tipo di dati**        | **Descrizione**                                                                                                                                                                                                                                                                                                                                                |
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Stringhe              | I tipi di dati stringa sono delimitati da spazi vuoti iniziali e finali e virgolette. MCI rimuove le virgolette singole da una stringa. Per inserire le virgolette in una stringa, utilizzare un set di due virgolette in cui si desidera incorporare le virgolette. Per usare una stringa vuota, usare due virgolette delimitate da spazi vuoti iniziali e finali. |
| Integer long con segno | I tipi di dati long integer con segno sono delimitati da spazi vuoti iniziali e finali. Se non diversamente specificato, i numeri interi possono essere positivi o negativi. Se si utilizzano numeri interi negativi, è consigliabile non separare il segno meno e la prima cifra con uno spazio.                                                                                                    |
| Rettangoli           | I tipi di dati Rectangle sono un elenco ordinato di quattro valori short con segno. Lo spazio vuoto delimita questo tipo di dati e separa ogni intero nell'elenco.                                                                                                                                                                                                              |



 

 

 