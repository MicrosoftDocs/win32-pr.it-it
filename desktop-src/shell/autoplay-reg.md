---
description: In molte situazioni potrebbe essere necessario disabilitare temporaneamente o in modo permanente l'avvio automatico.
ms.assetid: 5e65a3d8-04b9-46ba-b4e5-a976e1923bfd
title: Abilitazione e disabilitazione dell'esecuzione automatica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a567f50db75cd129346e193e66ba0ae5f74fa955
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401626"
---
# <a name="enabling-and-disabling-autorun"></a>Abilitazione e disabilitazione dell'esecuzione automatica

In molte situazioni potrebbe essere necessario disabilitare temporaneamente o in modo permanente l'avvio automatico. Ad esempio, l'esecuzione automatica potrebbe interferire con il funzionamento di un'applicazione in esecuzione e deve essere disabilitata per la durata. Il sistema offre diversi modi per disabilitare l'esecuzione automatica.

-   [Eliminazione automatica a livello di codice](#suppressing-autorun-programmatically)
-   [Uso del registro di sistema per disabilitare l'esecuzione automatica](#using-the-registry-to-disable-autorun)
-   [AutoRun per altri tipi di supporti di archiviazione](#autorun-for-other-types-of-storage-media)

## <a name="suppressing-autorun-programmatically"></a>Eliminazione automatica a livello di codice

Esistono diverse situazioni in cui potrebbe essere necessario disattivare l'esecuzione automatica a livello di codice. Di seguito sono riportati due esempi:

-   L'applicazione dispone di un programma di installazione che richiede all'utente di inserire un altro disco che potrebbe contenere un file Autorun. inf.
-   Durante il funzionamento dell'applicazione, l'utente potrebbe dover inserire un altro disco che potrebbe contenere un file Autorun. inf.

In entrambi i casi, in genere non si vuole avviare un'altra applicazione mentre è in corso l'originale.

Gli utenti possono disattivare manualmente l'esecuzione automatica tenendo premuto il tasto MAIUSC quando si inserisce il CD-ROM. Tuttavia, in genere è preferibile gestire questa operazione a livello di codice anziché a seconda dell'utente.

Con i sistemi con shell [versione 4,70](versions.md) e successive, Windows invia un messaggio "QueryCancelAutoPlay" alla finestra in primo piano. L'applicazione può rispondere a questo messaggio per disattivare l'esecuzione automatica. Questo approccio viene usato dalle utilità di sistema, ad esempio la finestra di dialogo [Apri](../dlgbox/open-and-save-as-dialog-boxes.md) comune, per disabilitare l'esecuzione automatica.

Nei frammenti di codice seguenti viene illustrato come impostare e gestire questo messaggio. L'applicazione deve essere in esecuzione nella finestra in primo piano. Per prima cosa, registrare "QueryCancelAutoPlay" come messaggio di Windows:


```C++
uMessage = RegisterWindowMessage(TEXT("QueryCancelAutoPlay"));
```



Per ricevere questo messaggio, la finestra dell'applicazione deve essere in primo piano. Il gestore di messaggi deve restituire **true** per annullare Autorun e **false** per abilitarlo. Il frammento di codice seguente illustra come usare questo messaggio per disabilitare l'esecuzione automatica.


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



Se l'applicazione usa una finestra di dialogo e deve rispondere a un messaggio "QueryCancelAutoPlay", non può semplicemente restituire **true** o **false**. Chiamare invece [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) con *NIndex* impostato su **DWL \_ MSGRESULT**. Impostare il parametro *dwNewLong* su **true** per annullare Autorun e **false** per abilitarlo. Ad esempio, la routine della finestra di dialogo di esempio seguente annulla l'esecuzione automatica quando riceve un messaggio "QueryCancelAutoPlay".


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



## <a name="using-the-registry-to-disable-autorun"></a>Uso del registro di sistema per disabilitare l'esecuzione automatica

Sono disponibili due valori del registro di sistema che possono essere usati per disabilitare in modo permanente AutoRun: NoDriveAutoRun e NoDriveTypeAutoRun. Il primo valore Disabilita l'esecuzione automatica per le lettere di unità specificate e la seconda disabilita l'esecuzione automatica per una classe di unità. Se uno di questi valori è impostato su Disabilita AutoRun per un particolare dispositivo, sarà disabilitato. Per ulteriori informazioni sulla disabilitazione della funzionalità di AutoRun, vedere l'articolo della Knowledge base [come disabilitare la funzionalità di avvio automatico di Windows](https://support.microsoft.com/kb/967715) . Questo articolo elenca i diversi aggiornamenti che è necessario avere installato per disabilitare correttamente la funzionalità di avvio automatico.

> [!Note]  
> I valori NoDriveAutoRun e NoDriveTypeAutoRun devono essere modificati solo dagli amministratori di sistema per modificare il valore dell'intero sistema a scopo di test o amministrativo. Le applicazioni non devono modificare questi valori, perché non è possibile ripristinare i valori originali in modo affidabile.

 

Il valore NoDriveAutoRun Disabilita l'esecuzione automatica per le lettere di unità specificate. Si tratta di un \_ valore di dati reg DWORD, disponibile nella chiave seguente:

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
                  Explorer
```

Il primo bit del valore corrisponde all'unità a:, il secondo a B: e così via. Per disabilitare l'esecuzione automatica per una o più lettere di unità, impostare i bit corrispondenti. Per disabilitare ad esempio le unità A: e C:, impostare NoDriveAutoRun su `0x00000005` .

Il valore NoDriveTypeAutoRun Disabilita l'esecuzione automatica per una classe di unità. Si tratta di un \_ valore reg DWORD o di dati binari reg a 4 byte \_ , disponibile nella stessa chiave.

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
                  Explorer
```

Impostando i bit del primo byte di questo valore, è possibile escludere unità diverse dall'utilizzo dell'AutoRun.

Nella tabella seguente vengono fornite le costanti bits e maschera di bit, che possono essere impostate nel primo byte di NoDriveTypeAutoRun per disabilitare l'esecuzione automatica per un determinato tipo di unità. Per rendere effettive le modifiche, è necessario riavviare Esplora risorse.



| Numero bit | Costante maschera di maschera      | Descrizione                                             |
|------------|-----------------------|---------------------------------------------------------|
| 0x04       | **UNITÀ \_ rimuovibile** | Il disco può essere rimosso dall'unità, ad esempio un disco floppy. |
| 0x08       | **UNITÀ \_ fissa**      | Non è possibile rimuovere il disco dall'unità (disco rigido).        |
| 0x10       | **UNITÀ \_ remota**     | Unità di rete.                                          |
| 0x20       | **UNITÀ \_ CD-ROM**      | Unità CD-ROM.                                           |
| 0x40       | **UNITÀ \_ ramdisk**    | Disco RAM.                                               |



 

## <a name="autorun-for-other-types-of-storage-media"></a>AutoRun per altri tipi di supporti di archiviazione

AutoRun è destinato principalmente alla distribuzione pubblica di applicazioni su CD-ROM e DVD-ROM e il suo utilizzo è sconsigliato per altri supporti di archiviazione. Tuttavia, è spesso utile abilitare l'esecuzione automatica su altri tipi di supporti di archiviazione rimovibili. Questa funzionalità viene in genere usata per semplificare il debug dei file AutoRun. inf. AutoRun funziona solo nei dispositivi di archiviazione rimovibili quando vengono soddisfatti i criteri seguenti:

-   Il dispositivo deve avere driver compatibili con l'avvio automatico. Per essere compatibile con l'AutoRun, un driver deve notificare al sistema che è stato inserito un disco inviando un messaggio [**WM \_ DEVICECHANGE**](../devio/wm-devicechange.md) .
-   La directory radice del supporto inserito deve contenere un file Autorun. inf.
-   L'AutoRun del dispositivo non deve essere disabilitato tramite il [Registro di sistema](#using-the-registry-to-disable-autorun).
-   L'applicazione in primo piano non ha [eliminato](#suppressing-autorun-programmatically) l'autorun.

> [!Note]  
> Questa funzionalità non deve essere utilizzata per distribuire applicazioni su supporti rimovibili. Poiché l'implementazione dell'AutoRun su supporti rimovibili fornisce un modo semplice per diffondere i virus dei computer, gli utenti devono essere sospetti di qualsiasi disco floppy distribuito pubblicamente che contenga un file Autorun. inf.

 

In genere, l'esecuzione automatica viene avviata automaticamente, ma può anche essere avviata manualmente. Se il dispositivo soddisfa i criteri elencati in precedenza, nel menu di scelta rapida della lettera di unità sarà incluso un comando **AutoPlay** . Per eseguire l'esecuzione automatica manualmente, fare clic con il pulsante destro del mouse sull'icona dell'unità e scegliere **AutoPlay** dal menu di scelta rapida oppure fare doppio clic sull'icona dell'unità. Se i driver non sono compatibili con l'AutoRun, il menu di scelta rapida non avrà un elemento **AutoPlay** e non sarà possibile avviare Autorun.

I driver compatibili con l'AutoRun sono forniti con alcune unità disco rimovibili, oltre ad altri tipi di supporti rimovibili, ad esempio schede CompactFlash. AutoRun funziona anche con le unità di rete di cui è stato eseguito il mapping a una lettera di unità con Esplora risorse o montata con [Microsoft Management Console (MMC)](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page). Come per l'hardware montato, un'unità di rete montata deve avere un file Autorun. inf nella directory radice e non deve essere disabilitata tramite il [Registro di sistema](#using-the-registry-to-disable-autorun).

 

 
