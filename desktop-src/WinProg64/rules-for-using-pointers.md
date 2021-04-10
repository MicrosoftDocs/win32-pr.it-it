---
title: Regole per l'utilizzo di puntatori
description: Il porting del codice per la compilazione sia per Microsoft Windows a 32 che a 64 bit è molto semplice. È necessario seguire solo alcune semplici regole per il cast dei puntatori e usare i nuovi tipi di dati nel codice. Di seguito sono riportate le regole per la manipolazione dei puntatori.
ms.assetid: 4c38bee2-fa1c-493f-a12d-e673df4d4895
keywords:
- regole per l'utilizzo di puntatori programmazione Windows a 64 bit
- manipolazione del puntatore programmazione Windows a 64 bit
- puntatori di cast a 64 bit programmazione Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 318ff5beed6dc90bd49b6b293131e17db6f92f6b
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "103963527"
---
# <a name="rules-for-using-pointers"></a>Regole per l'utilizzo di puntatori

Il porting del codice per la compilazione sia per Microsoft Windows a 32 che a 64 bit è molto semplice. È necessario seguire solo alcune semplici regole per il cast dei puntatori e usare i nuovi tipi di dati nel codice. Di seguito sono riportate le regole per la manipolazione dei puntatori.

1.  Non eseguire il cast di puntatori a **int**, **Long**, **ULONG** o **DWORD**.

    Se è necessario eseguire il cast di un puntatore per testare alcuni bit, impostare o deselezionare bits oppure modificare il contenuto, utilizzare il tipo **uint \_ ptr** o **int \_ ptr** . Questi tipi sono tipi integrali che si adattano alle dimensioni di un puntatore per Windows a 32 e 64 bit (ad esempio, **ULONG** per windows a 32 bit e \_ Int64 per Windows a 64 bit). Si supponga, ad esempio, di dover trasferire il codice seguente:

    `ImageBase = (PVOID)((ULONG)ImageBase | 1);`

    Come parte del processo di porting, modificare il codice nel modo seguente:

    `ImageBase = (PVOID)((ULONG_PTR)ImageBase | 1);`

    Usare **uint \_ ptr** e **int \_ ptr** laddove appropriato (e se non si è certi che siano necessari, non vi è alcun danno per usarli solo nel caso). Non eseguire il cast dei puntatori ai tipi **ULONG**, **Long**, **int**, **uint** o **DWORD**.

    Si noti che **handle** è definito come **void \***, quindi typecasting un valore di **handle** a un valore **ULONG** per testare, impostare o deselezionare i 2 bit di ordine inferiore è un errore in Windows a 64 bit.

2.  Utilizzare la funzione **PtrToLong** o **PtrToUlong** per troncare i puntatori.

    Se è necessario troncare un puntatore a un valore a 32 bit, utilizzare la funzione **PtrToLong** o **PtrToUlong** (definita in Basetsd. h). Queste funzioni disabilitano l'avviso di troncamento del puntatore per la durata della chiamata.

    Usare queste funzioni con cautela. Dopo aver convertito una variabile puntatore usando una di queste funzioni, non usarla mai come puntatore. Queste funzioni troncano i bit 32 superiori di un indirizzo, che in genere sono necessari per accedere alla memoria a cui fa riferimento originariamente il puntatore. L'uso di queste funzioni senza un'attenta considerazione produrrà un codice fragile.

3.  Prestare attenzione quando si usano \_ i valori del puntatore 32 nel codice che può essere compilato come codice a 64 bit. Il compilatore estenderà il puntatore quando verrà assegnato a un puntatore nativo nel codice a 64 bit, senza estendere il puntatore a zero.
4.  Prestare attenzione quando si usano \_ i valori del puntatore 64 nel codice che può essere compilato come codice a 32 bit. Il compilatore estenderà il puntatore nel codice a 32 bit, senza estendere il puntatore.
5.  Prestare attenzione usando i parametri OUT.

    Si supponga, ad esempio, di avere una funzione definita nel modo seguente:

    `void func( OUT PULONG *PointerToUlong );`

    Non chiamare questa funzione come indicato di seguito.

    ``` syntax
    ULONG ul;
    PULONG lp;
    func((PULONG *)&ul);
    lp = (PULONG)ul;
    ```

    Usare invece la chiamata seguente.

    ``` syntax
    PULONG lp;
    func(&lp);
    ```

    Typecasting &UL a **PULONG \*** impedisce un errore del compilatore, ma la funzione scriverà un valore di puntatore a 64 bit nella memoria &UL. Questo codice funziona su Windows a 32 bit, ma provocherà il danneggiamento dei dati in Windows a 64 bit e sarà un danneggiamento difficile da trovare. Il risultato finale è che i trucchi con il codice C non sono semplici, ma è preferibile.

6.  Prestare attenzione alle interfacce polimorfiche.

    Non creare funzioni che accettano parametri **DWORD** per i dati polimorfici. Se i dati possono essere un puntatore o un valore integrale, utilizzare il \_ tipo uint PTR o **PVOID** .

    Ad esempio, non creare una funzione che accetta una matrice di parametri di eccezione tipizzati come valori **DWORD** . La matrice deve essere una matrice di **valori \_ ptr DWORD** . Gli elementi della matrice possono pertanto conservare indirizzi o valori integrali a 32 bit. La regola generale è che se il tipo originale è **DWORD** ed è necessario che la larghezza del puntatore venga convertita in valore **\_ ptr DWORD** . Per questo motivo sono presenti tipi di precisione puntatore corrispondenti. Se si dispone di codice che usa **DWORD**, **ULONG** o altri tipi a 32 bit in modo polimorfico (ovvero si vuole che il parametro o il membro della struttura contenga un indirizzo), usare **uint \_ ptr** al posto del tipo corrente.

7.  Utilizzare le nuove funzioni della classe di finestra.

    Se si dispone di dati privati di finestra o di classe che contengono puntatori, il codice dovrà usare le nuove funzioni seguenti:

    -   [**GetClassLongPtr**](/windows/win32/api/winuser/nf-winuser-getclasslongptra)
    -   [**GetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-getwindowlongptra)
    -   [**SetClassLongPtr**](/windows/win32/api/winuser/nf-winuser-setclasslongptra)
    -   [**SetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra)

    Queste funzioni possono essere usate in Windows a 32 e 64 bit, ma sono necessarie nelle finestre a 64 bit. Preparare la transizione usando ora queste funzioni.

    Inoltre, è necessario accedere a puntatori o handle in dati privati della classe usando le nuove funzioni in Windows a 64 bit. Per facilitare la ricerca di questi casi, gli indici seguenti non sono definiti in winuser. h durante una compilazione a 64 bit:

    -   GWL \_ WndProc
    -   \_HINSTANCE GWL
    -   \_HWDPARENT GWL
    -   \_UserData GWL

    Al contrario, winuser. h definisce i nuovi indici seguenti:

    -   GWLP \_ WndProc
    -   \_HINSTANCE GWLP
    -   \_HWNDPARENT GWLP
    -   \_UserData GWLP
    -   \_ID GWLP

    Ad esempio, il codice seguente non viene compilato:

    `SetWindowLong(hWnd, GWL_WNDPROC, (LONG)MyWndProc);`

    Deve essere modificato come segue:

    `SetWindowLongPtr(hWnd, GWLP_WNDPROC, (LONG_PTR)MyWndProc);`

    Quando si imposta il membro **cbWndExtra** della struttura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) , assicurarsi di riservare spazio sufficiente per i puntatori. Se, ad esempio, si stanno attualmente conservando i byte sizeof (DWORD) per un valore di puntatore, riservare i byte sizeof (DWORD \_ ptr).

8.  Accedere a tutti i dati della finestra e della classe usando l' **\_ offset del campo**.

    È frequente accedere ai dati della finestra usando offset hardcoded. Questa tecnica non è portabile in Windows a 64 bit. Per rendere portabile il codice, accedere ai dati della finestra e della classe usando la macro **\_ offset campo** . Non presupporre che il secondo puntatore abbia un offset pari a 4.

9.  I tipi **lParam**, **wParam** e **LRESULT** cambiano dimensione con la piattaforma.

    Quando si compila codice a 64 bit, questi tipi si espandono fino a 64 bit, perché in genere contengono puntatori o tipi integrali. Non combinare questi valori con valori **DWORD**, **ULONG**, **uint**, **int**, **int** o **Long** . Esaminare la modalità di utilizzo di questi tipi e assicurarsi di non troncare inavvertitamente i valori.

 

 