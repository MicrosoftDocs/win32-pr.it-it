---
title: Conformità RIGOROSa
description: Alcuni codici sorgente compilati correttamente potrebbero generare messaggi di errore quando si Abilita il controllo del tipo STRICT.
ms.assetid: 88368fec-b375-4ad0-aa13-ffadf0338a44
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02d04c3a849dc62647758e3515728e3dd3f65dcb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399288"
---
# <a name="strict-compliance"></a>Conformità RIGOROSa

Alcuni codici sorgente compilati correttamente potrebbero generare messaggi di errore quando si Abilita il controllo del tipo **strict** . Le sezioni seguenti descrivono i requisiti minimi per la compilazione del codice quando è abilitata la funzionalità **strict** . Sono consigliate procedure aggiuntive, in particolare per produrre codice portabile.

## <a name="general-requirements"></a>Requisiti generali

Il requisito principale è che è necessario dichiarare i tipi di handle corretti e i puntatori a funzione anziché basarsi su tipi più generali. Non è possibile usare un tipo di handle dove ne è previsto un altro. Ciò significa anche che potrebbe essere necessario modificare le dichiarazioni di funzione e utilizzare più cast di tipo.

Per ottenere risultati ottimali, è consigliabile utilizzare il tipo di **handle** generico solo quando necessario.

## <a name="declaring-functions-within-your-application"></a>Dichiarazione di funzioni all'interno dell'applicazione

Verificare che tutte le funzioni dell'applicazione siano dichiarate. L'inserimento di tutte le dichiarazioni di funzione in un file di inclusione è consigliato perché è possibile analizzare facilmente le dichiarazioni e cercare i tipi di parametro e restituiti che devono essere modificati.

Se si usa l'opzione del compilatore **/ZG** per creare i file di intestazione per le funzioni, tenere presente che si otterranno risultati diversi a seconda che sia stato abilitato il controllo del tipo **strict** . Con **strict** disabled, tutti i tipi di handle generano lo stesso tipo di base. Con **strict** abilitato, generano tipi di base diversi. Per evitare conflitti, è necessario ricreare il file di intestazione ogni volta che si Abilita o si disabilita **strict** oppure modificare il file di intestazione per usare i tipi **HWND**, **HDC**, **handle** e così via, anziché i tipi di base.

Qualsiasi dichiarazione di funzione copiata da Windows. h nel codice sorgente potrebbe essere stata modificata e la dichiarazione locale potrebbe non essere aggiornata. Rimuovere la dichiarazione locale.

## <a name="types-that-require-casts"></a>Tipi che richiedono cast

Alcune funzioni dispongono di parametri o tipi restituiti generici. La funzione [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) , ad esempio, restituisce dati che possono essere un numero qualsiasi di tipi, a seconda del contesto. Quando si visualizza una di queste funzioni nel codice sorgente, assicurarsi di utilizzare il cast del tipo corretto e che sia il più possibile specifico. L'elenco seguente è un esempio di queste funzioni.

-   [**LocalLock**](/windows/desktop/api/winbase/nf-winbase-locallock)
-   [**GlobalLock**](/windows/desktop/api/winbase/nf-winbase-globallock)
-   [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga)
-   [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga)
-   [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage)
-   [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
-   [**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea)

Quando si chiama [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage), [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)o [**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea), è innanzitutto necessario eseguire il cast del risultato al **tipo \_ uint PTR**. È necessario eseguire una procedura simile per qualsiasi funzione che restituisce un valore **LRESULT** o **Long \_ ptr** , in cui il risultato contiene un handle. Questa operazione è necessaria per la scrittura di codice portabile, in quanto le dimensioni di un handle variano a seconda della versione di Windows. Il cast (**uint \_ ptr**) garantisce una corretta conversione. Il codice seguente illustra un esempio in cui **SendMessage** restituisce un handle a un pennello:


```C++
HBRUSH hbr;

hbr = (HBRUSH)(UINT_PTR)SendMessage(hwnd, WM_CTLCOLOR, ..., ...);
```



Il parametro **CreateWindow** e **CreateWindowEx** *HMENU* viene talvolta usato per passare un identificatore di controllo Integer (ID). In questo caso, è necessario eseguire il cast dell'ID a un tipo **HMENU** :


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

Per sfruttare al massimo i vantaggi derivanti dal controllo **rigoroso** dei tipi, è necessario seguire altre linee guida. Se si apportano le modifiche seguenti, il codice sarà più portatile nelle versioni future di Windows.

I tipi **wParam**, **lParam**, **LRESULT** e **LPVOID** sono *tipi di dati polimorfici*. Contengono diversi tipi di dati in momenti diversi, anche quando è abilitato il controllo di tipo **strict** . Per sfruttare i vantaggi del controllo dei tipi, è consigliabile eseguire il cast dei valori di questi tipi il prima possibile. Si noti che i cracker del messaggio riesegue automaticamente il cast di *wParam* e *lParam* in modo portatile.

Prestare particolare attenzione per distinguere i tipi **hmodule** e **HINSTANCE** . Anche se **strict** è abilitato, vengono definiti come lo stesso tipo di base. La maggior parte delle funzioni di gestione dei moduli kernel usa tipi **HINSTANCE** , ma esistono alcune funzioni che restituiscono o accettano solo tipi **hmodule** .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Disabilitazione di STRICT](disabling-strict.md)
</dt> <dt>

[Abilitazione di STRICT](enabling-strict.md)
</dt> </dl>

 

 