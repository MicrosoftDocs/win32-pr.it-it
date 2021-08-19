---
title: Conformità STRICT
description: Un codice sorgente compilato correttamente potrebbe generare messaggi di errore quando si abilita il controllo dei tipi STRICT.
ms.assetid: 88368fec-b375-4ad0-aa13-ffadf0338a44
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29baee071bd8d7c236ec5f2f99d1dff11aeac37deb44b0d8a6254325c9a75df0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117928146"
---
# <a name="strict-compliance"></a>Conformità STRICT

Un codice sorgente compilato correttamente potrebbe generare messaggi di errore quando si abilita il controllo dei tipi **STRICT.** Le sezioni seguenti descrivono i requisiti minimi per la compilazione del codice quando **è abilitato STRICT.** Sono consigliati passaggi aggiuntivi, in particolare per produrre codice portabile.

## <a name="general-requirements"></a>Requisiti generali

Il requisito principale è che è necessario dichiarare tipi di handle e puntatori a funzione corretti anziché basarsi su tipi più generali. Non è possibile usare un tipo di handle in cui è previsto un altro. Ciò significa anche che potrebbe essere necessario modificare le dichiarazioni di funzione e usare più cast di tipo.

Per ottenere risultati ottimali, il **tipo HANDLE** generico deve essere usato solo quando necessario.

## <a name="declaring-functions-within-your-application"></a>Dichiarazione di funzioni all'interno dell'applicazione

Assicurarsi che tutte le funzioni dell'applicazione siano dichiarate. È consigliabile inserire tutte le dichiarazioni di funzione in un file di inclusione perché è possibile analizzare facilmente le dichiarazioni e cercare i tipi di parametro e restituiti che devono essere modificati.

Se si usa l'opzione del compilatore **/Zg** per creare file di intestazione per le funzioni, tenere presente che si otterrà risultati diversi a seconda che sia stato abilitato il controllo dei tipi **STRICT.** Con **STRICT disabilitato,** tutti i tipi di handle generano lo stesso tipo di base. Con **STRICT** abilitato, generano tipi di base diversi. Per evitare conflitti, è necessario creare di nuovo il file di intestazione ogni volta che si abilita o disabilita **STRICT** oppure modificare il file di intestazione in modo da usare i tipi **HWND,** **HDC,** **HANDLE** e così via, anziché i tipi di base.

Le dichiarazioni di funzione copiate da Windows.h nel codice sorgente potrebbero essere state modificate e la dichiarazione locale potrebbe non essere aggiornata. Rimuovere la dichiarazione locale.

## <a name="types-that-require-casts"></a>Tipi che richiedono cast

Alcune funzioni hanno parametri o tipi restituiti generici. Ad esempio, la [**funzione SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) restituisce dati che possono essere un numero qualsiasi di tipi, a seconda del contesto. Quando viene visualizzata una di queste funzioni nel codice sorgente, assicurarsi di usare il cast di tipo corretto e che sia il più specifico possibile. L'elenco seguente è un esempio di queste funzioni.

-   [**LocalLock**](/windows/desktop/api/winbase/nf-winbase-locallock)
-   [**GlobalLock**](/windows/desktop/api/winbase/nf-winbase-globallock)
-   [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga)
-   [**Setwindowlong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga)
-   [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage)
-   [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
-   [**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea)

Quando si chiama [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage), [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)o [**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea), è prima necessario eseguire il cast del risultato al tipo **UINT \_ PTR**. È necessario eseguire passaggi simili per qualsiasi funzione che restituisce un **valore LRESULT** o **LONG \_ PTR,** in cui il risultato contiene un handle. Questa operazione è necessaria per la scrittura di codice portabile perché le dimensioni di un handle variano a seconda della versione di Windows. Il cast (**UINT \_ PTR**) garantisce la conversione corretta. Il codice seguente illustra un esempio in cui **SendMessage** restituisce un handle a un pennello:


```C++
HBRUSH hbr;

hbr = (HBRUSH)(UINT_PTR)SendMessage(hwnd, WM_CTLCOLOR, ..., ...);
```



Il parametro *hmenu* **CreateWindow** e **CreateWindowEx** viene talvolta usato per passare un identificatore di controllo integer (ID). In questo caso, è necessario eseguire il cast dell'ID a un **tipo HMENU:**


```C++
HWND hwnd;
int id;

hwnd = CreateWindow(
        TEXT("Button"), TEXT("OK"), BS_PUSHBUTTON,
        x, y, cx, cy, hwndParent,
        (HMENU)id,    // Cast required here
        hinst,
        NULL);
```



## <a name="additional-considerations"></a>Ulteriori considerazioni

Per ottenere il massimo vantaggio dal controllo dei tipi **STRICT,** è necessario seguire altre linee guida. Il codice sarà più portabile nelle versioni future Windows se si apportano le modifiche seguenti.

I tipi **WPARAM**, **LPARAM**, **LRESULT** e **LPVOID** sono *tipi di dati polimorfici*. Contengono tipi diversi di dati in momenti diversi, anche quando **è abilitato il controllo** dei tipi STRICT. Per ottenere il vantaggio del controllo dei tipi, è necessario eseguire il cast di valori di questi tipi appena possibile. Si noti che i cracker dei messaggi recast *automatico wParam* *e lParam* per l'utente in modo portabile.

Fare particolare attenzione a distinguere **i tipi HMODULE** **e HINSTANCE.** Anche con **STRICT** abilitato, vengono definiti come lo stesso tipo di base. La maggior parte delle funzioni di gestione dei moduli del kernel usa tipi **HINSTANCE,** ma esistono alcune funzioni che restituiscono o accettano solo **tipi HMODULE.**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Disabilitazione di STRICT](disabling-strict.md)
</dt> <dt>

[Abilitazione di STRICT](enabling-strict.md)
</dt> </dl>

 

 