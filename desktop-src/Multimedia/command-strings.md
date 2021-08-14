---
title: Stringhe di comando
description: Stringhe di comando
ms.assetid: ca9ca153-f2bf-45ed-84e6-44e86e8efaed
keywords:
- stringhe di comando MCI, informazioni su
- stringhe di comando MCI, sintassi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08f3638271dd004db13fe3ee2f0517eef0c1d2fe72be93da37a73f47e6666212
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807831"
---
# <a name="command-strings"></a>Stringhe di comando

Per inviare un comando stringa a un dispositivo MCI, usare la funzione [**mciSendString,**](/previous-versions//dd757161(v=vs.85)) che include i parametri per il comando stringa e un buffer per le informazioni restituite.

La **funzione mciSendString** restituisce zero in caso di esito positivo. Se la funzione ha esito negativo, la parola di ordine basso del valore restituito contiene un codice di errore. È possibile passare questo codice di errore alla [**funzione mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) per ottenere una descrizione testuale dell'errore.

## <a name="syntax-of-command-strings"></a>Sintassi delle stringhe di comando

Le stringhe di comando MCI usano una sintassi di modificatori verbo-oggetto coerente. Ogni stringa di comando include un comando, un identificatore di dispositivo e argomenti di comando. Gli argomenti sono facoltativi per alcuni comandi e obbligatori per altri.

Una stringa di comando ha il formato seguente:

*argomenti \_ dell'ID del dispositivo di comando*

Questi componenti contengono le informazioni seguenti:

-   Il *comando* specifica un comando MCI, ad esempio [**open**](open.md), [**close**](close.md)o [**play**](play.md).
-   *\_ L'ID dispositivo* identifica un'istanza di un driver MCI. *\_ L'ID dispositivo* viene creato all'apertura del dispositivo.
-   Gli *argomenti* specificano i flag e le variabili usati dal comando. I flag sono parole chiave riconosciute con il comando MCI. Le variabili sono numeri o stringhe che si applicano al comando o al flag MCI.

    Ad esempio, il **comando play** usa gli argomenti "from *position"* e "to *position"* per indicare le posizioni da cui iniziare e terminare la riproduzione. È possibile elencare i flag usati con un comando in qualsiasi ordine. Quando si usa un flag a cui è associata una variabile, è necessario specificare un valore per la variabile.

    Gli argomenti del comando non specificati (e facoltativi) presuppongono un valore predefinito.

La funzione di esempio seguente invia [**il comando play**](play.md) con i flag "from" e "to".


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

È possibile usare i tipi di dati seguenti per le variabili in una stringa di comando.



| **Tipo di dati**        | **Descrizione**                                                                                                                                                                                                                                                                                                                                                |
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Stringhe              | I tipi di dati stringa sono delimitati da spazi vuoti iniziali e finali e virgolette. MCI rimuove le virgolette singole da una stringa. Per inserire le virgolette in una stringa, usare un set di due virgolette in cui si desidera incorporare le virgolette. Per usare una stringa vuota, usare due virgolette delimitate da spazi vuoti iniziali e finali. |
| Interi lunghi con segno | I long integer dati con segno sono delimitati da spazi vuoti iniziali e finali. Se non diversamente specificato, i numeri interi possono essere positivi o negativi. Se si usano numeri interi negativi, non è necessario separare il segno meno e la prima cifra con uno spazio.                                                                                                    |
| Rettangoli           | I tipi di dati Rectangle sono un elenco ordinato di quattro valori short con segno. Lo spazio vuoto delimita questo tipo di dati e separa ogni numero intero nell'elenco.                                                                                                                                                                                                              |



 

 

 