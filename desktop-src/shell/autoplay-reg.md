---
description: In molte situazioni potrebbe essere necessario disabilitare temporaneamente o in modo permanente l'esecuzione automatica.
ms.assetid: 5e65a3d8-04b9-46ba-b4e5-a976e1923bfd
title: Abilitazione e disabilitazione dell'esecuzione automatica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbd14a1dfd3aadb94f3586dec783ea6d394f717f500b5ac103c65fcb813baf14
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090781"
---
# <a name="enabling-and-disabling-autorun"></a>Abilitazione e disabilitazione dell'esecuzione automatica

In molte situazioni potrebbe essere necessario disabilitare temporaneamente o in modo permanente l'esecuzione automatica. Ad esempio, l'esecuzione automatica potrebbe interferire con il funzionamento di un'applicazione in esecuzione e deve essere disabilitata per la durata. Il sistema offre diversi modi per disabilitare l'esecuzione automatica.

-   [Eliminazione dell'esecuzione automatica a livello di codice](#suppressing-autorun-programmatically)
-   [Uso del Registro di sistema per disabilitare l'esecuzione automatica](#using-the-registry-to-disable-autorun)
-   [Esecuzione automatica per altri tipi di Archiviazione multimediali](#autorun-for-other-types-of-storage-media)

## <a name="suppressing-autorun-programmatically"></a>Eliminazione dell'esecuzione automatica a livello di codice

Esistono diverse situazioni in cui potrebbe essere necessario eliminare l'esecuzione automatica a livello di codice. Di seguito sono riportati due esempi:

-   L'applicazione ha un programma di installazione che richiede all'utente di inserire un altro disco che può contenere un file Autorun.inf.
-   Durante il funzionamento dell'applicazione, l'utente potrebbe dover inserire un altro disco che potrebbe contenere un file Autorun.inf.

In entrambi i casi, in genere non si vuole avviare un'altra applicazione mentre l'originale è in corso.

Gli utenti possono eliminare manualmente l'esecuzione automatica tenendo premuto MAIUSC quando inseriscono il CD-ROM. Tuttavia, è in genere preferibile gestire questa operazione a livello di codice anziché a seconda dell'utente.

Con i sistemi con Shell [versione 4.70](versions.md) e successive, Windows un messaggio "QueryCancelAutoPlay" alla finestra in primo piano. L'applicazione può rispondere a questo messaggio per eliminare l'esecuzione automatica. Questo approccio viene usato dalle utilità di sistema, ad esempio la [finestra](../dlgbox/open-and-save-as-dialog-boxes.md) di dialogo Apri comune per disabilitare l'esecuzione automatica.

I frammenti di codice seguenti illustrano come configurare e gestire questo messaggio. L'applicazione deve essere in esecuzione nella finestra in primo piano. Per prima cosa, registrare "QueryCancelAutoPlay" come Windows messaggio:


```C++
uMessage = RegisterWindowMessage(TEXT("QueryCancelAutoPlay"));
```



La finestra dell'applicazione deve essere in primo piano per ricevere questo messaggio. Il gestore di messaggi deve restituire **TRUE per** annullare l'esecuzione automatica e **FALSE** per abilitarlo. Il frammento di codice seguente illustra come usare questo messaggio per disabilitare l'esecuzione automatica.


```C++
UINT g_uQueryCancelAutoPlay = 0;

LRESULT WndProc(HWND hwnd, UINT uMsg,  WPARAM wParam, LPARAM lParam) 
{ 
    switch (uMsg) 
    { 
    ... 
    default: 
        if (!g_uQueryCancelAutoPlay)
        { 
            g_uQueryCancelAutoPlay = RegisterWindowMessage(TEXT("QueryCancelAutoPlay"));
        } 
        if (uMsg && uMsg == g_uQueryCancelAutoPlay)
        { 
            return TRUE;       // Cancel AutoRun
        }
    }
}
```



Se l'applicazione usa una finestra di dialogo e deve rispondere a un messaggio "QueryCancelAutoPlay", non può semplicemente restituire **TRUE** o **FALSE.** Chiamare invece [**SetWindowLong con**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) *nIndex* impostato su **DWL \_ MSGRESULT**. Impostare il *parametro dwNewLong* su **TRUE per** annullare l'esecuzione automatica e **FALSE** per abilitarlo. Ad esempio, la procedura della finestra di dialogo di esempio seguente annulla l'esecuzione automatica quando riceve un messaggio "QueryCancelAutoPlay".


```C++
UINT g_uQueryCancelAutoPlay = 0;

BOOL DialogProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    switch (uMsg) 
    { 
    ...
    default: 
        if (!g_uQueryCancelAutoPlay)
        {
            g_uQueryCancelAutoPlay = RegisterWindowMessage(TEXT("QueryCancelAutoPlay"));
        } 
        if (uMsg == g_uQueryCancelAutoPlay) 
        {
            SetWindowLong(hDlg, DWL_MSGRESULT, TRUE);          
            return 1;               
        }
    } 
```



## <a name="using-the-registry-to-disable-autorun"></a>Uso del Registro di sistema per disabilitare l'esecuzione automatica

Esistono due valori del Registro di sistema che possono essere usati per disabilitare in modo permanente l'esecuzione automatica: NoDriveAutoRun e NoDriveTypeAutoRun. Il primo valore disabilita l'esecuzione automatica per le lettere di unità specificate e il secondo disabilita l'esecuzione automatica per una classe di unità. Se uno di questi valori è impostato per disabilitare l'esecuzione automatica per un dispositivo specifico, verrà disabilitato. Per altre informazioni sulla disabilitazione della funzionalità di esecuzione automatica, vedere l'articolo Knowledge Base come disabilitare la funzionalità di esecuzione automatica [in Windows.](https://support.microsoft.com/kb/967715) Questo articolo elenca i diversi aggiornamenti che è necessario aver installato per disabilitare correttamente la funzionalità di esecuzione automatica.

> [!Note]  
> I valori NoDriveAutoRun e NoDriveTypeAutoRun devono essere modificati solo dagli amministratori di sistema per modificare il valore per l'intero sistema a scopo di test o amministrativo. Le applicazioni non devono modificare questi valori, perché non è possibile ripristinarli in modo affidabile ai valori originali.

 

Il valore NoDriveAutoRun disabilita l'esecuzione automatica per le lettere di unità specificate. Si tratta di un valore \_ di dati REG DWORD, disponibile nella chiave seguente:

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
                  Explorer
```

Il primo bit del valore corrisponde all'unità A:, il secondo a B:e così via. Per disabilitare l'esecuzione automatica per una o più lettere di unità, impostare i bit corrispondenti. Ad esempio, per disabilitare le unità A: e C:, impostare NoDriveAutoRun su `0x00000005` .

Il valore NoDriveTypeAutoRun disabilita l'esecuzione automatica per una classe di unità. Si tratta di un valore di dati REG DWORD o REG BINARY a \_ 4 \_ byte, che si trova nella stessa chiave.

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
                  Explorer
```

Impostando i bit del primo byte di questo valore, è possibile escludere unità diverse dall'uso dell'esecuzione automatica.

Nella tabella seguente sono riportati i bit e le costanti di maschera di bit, che possono essere impostati nel primo byte di NoDriveTypeAutoRun per disabilitare l'esecuzione automatica per un particolare tipo di unità. È necessario riavviare Windows Explorer prima che le modifiche si apportare.



| Numero di bit | Costante maschera di bit      | Descrizione                                             |
|------------|-----------------------|---------------------------------------------------------|
| 0x04       | **UNITÀ \_ RIMOVIBILE** | Il disco può essere rimosso dall'unità , ad esempio un disco floppy. |
| 0x08       | **UNITÀ \_ FISSA**      | Impossibile rimuovere il disco dall'unità (disco rigido).        |
| 0x10       | **UNITÀ \_ REMOTA**     | Unità di rete.                                          |
| 0x20       | **UNITÀ \_ CDROM**      | Unità CD-ROM.                                           |
| 0x40       | **UNITÀ \_ RAMDISK**    | Disco RAM.                                               |



 

## <a name="autorun-for-other-types-of-storage-media"></a>Esecuzione automatica per altri tipi di Archiviazione multimediali

L'esecuzione automatica è destinata principalmente alla distribuzione pubblica di applicazioni su CD-ROM e DVD-ROM e il suo uso è sconsigliato per altri supporti di archiviazione. Tuttavia, è spesso utile abilitare l'esecuzione automatica in altri tipi di supporti di archiviazione rimovibili. Questa funzionalità viene in genere usata per semplificare il debug dei file AutoRun.inf. L'esecuzione automatica funziona solo nei dispositivi di archiviazione rimovibili quando vengono soddisfatti i criteri seguenti:

-   Il dispositivo deve avere driver compatibili con l'esecuzione automatica. Per essere compatibile con l'esecuzione automatica, un driver deve notificare al sistema che è stato inserito un disco inviando un [**messaggio WM \_ DEVICECHANGE.**](../devio/wm-devicechange.md)
-   La directory radice del supporto inserito deve contenere un file Autorun.inf.
-   L'esecuzione automatica del dispositivo non deve essere disabilitata tramite il Registro [di sistema.](#using-the-registry-to-disable-autorun)
-   L'applicazione in primo piano non [ha eliminato l'esecuzione](#suppressing-autorun-programmatically) automatica.

> [!Note]  
> Questa funzionalità non deve essere usata per distribuire applicazioni su supporti rimovibili. Poiché l'implementazione dell'esecuzione automatica su supporti rimovibili offre un modo semplice per distribuire virus del computer, gli utenti devono essere sospetti di qualsiasi disco floppy distribuito pubblicamente che contiene un file Autorun.inf.

 

In genere, l'esecuzione automatica viene avviata automaticamente, ma può anche essere avviata manualmente. Se il dispositivo soddisfa i criteri elencati in precedenza, il menu di scelta rapida della lettera di unità includerà un **comando AutoPlay.** Per eseguire l'esecuzione automatica manualmente, fare clic con il pulsante destro del mouse sull'icona dell'unità e scegliere **AutoPlay** dal menu di scelta rapida oppure fare doppio clic sull'icona dell'unità. Se i driver non sono compatibili con l'esecuzione automatica, il menu di scelta rapida non avrà un elemento **AutoPlay** e non sarà possibile avviare l'esecuzione automatica.

I driver compatibili con l'esecuzione automatica sono forniti con alcune unità disco rimovibili, nonché altri tipi di supporti rimovibili, ad esempio schede CompactFlash. L'esecuzione automatica funziona anche con le unità di rete mappate a una lettera di unità con Windows Explorer o montate con [Microsoft Management Console (MMC).](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) Come per l'hardware montato, un'unità di rete montata deve avere un file Autorun.inf nella directory radice e non deve essere disabilitata tramite il Registro [di sistema](#using-the-registry-to-disable-autorun).

 

 
