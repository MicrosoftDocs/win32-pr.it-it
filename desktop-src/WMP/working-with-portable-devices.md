---
title: Uso di dispositivi portatili
description: Uso di dispositivi portatili
ms.assetid: 145ede07-a23b-486b-a561-9c87a48b72a8
keywords:
- Windows Media Player, dispositivi portatili
- Windows Media Player a oggetti, dispositivi portatili
- modello a oggetti, dispositivi portatili
- Windows Media Player ActiveX, dispositivi portatili
- ActiveX, dispositivi portatili
- Windows Media Player Controllo ActiveX per dispositivi mobili, dispositivi portatili
- Windows Media Player Dispositivi mobili, portatili
- dispositivi portatili, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34cbff16b293ac4ab438c1b018608497d2a61cdfa6fb727332d5b50a27de313c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117745507"
---
# <a name="working-with-portable-devices"></a>Uso di dispositivi portatili

Questa sezione descrive come usare un controllo Windows Media Player ActiveX remoto per lavorare con i dispositivi portatili.

Gli esempi di codice in questa sezione usano Active Template Library (ATL), ad esempio **CComPtr**.

## <a name="included-headers"></a>Intestazioni incluse

Per usare il codice in questa sezione, includere le intestazioni seguenti:


```C++
#include <atlbase.h>
#include <atlcom.h>
#include <atlwin.h>
#include <commctrl.h>
#include "wmp.h"
#include "wmpids.h"
```



## <a name="iwmpplayer-pointer"></a>Puntatore IWMPPlayer

Il **puntatore IWMPPlayer** viene archiviato in una variabile membro.


```C++
CComPtr<IWMPPlayer> m_spPlayer;
```



## <a name="devices-are-stored-in-an-array"></a>I dispositivi vengono archiviati in una matrice

Il codice di esempio accede alla variabile membro seguente, da dichiarare nell'intestazione del progetto:


```C++
IWMPSyncDevice **m_ppWMPDevices; // Points to the custom device array.
```



Il numero di dispositivi viene archiviato in una variabile membro.


```C++
int m_cDevices; // Count of devices.
```



## <a name="retrieving-a-device-pointer"></a>Recupero di un puntatore di dispositivo

Un puntatore a un dispositivo specifico viene recuperato tramite il relativo indice di matrice usando codice simile al seguente:


```C++
CComPtr<IWMPSyncDevice> spSyncDevice(m_ppWMPDevices[lIndex]);
```



Si noti che l'indice mostrato negli esempi precedenti non è l'indice di partnership per il dispositivo. È l'indice del dispositivo nella matrice personalizzata di dispositivi.

## <a name="cleaning-up"></a>Pulizia

Negli esempi viene utilizzata la funzione seguente per liberare la memoria nella matrice di dispositivi e rilasciare i puntatori a interfaccia:


```C++
void CMainDlg::FreeDeviceArray()
{
    if(m_ppWMPDevices)
    {
        for(long i = 0; i < m_cDevices; i++)
        {
            m_ppWMPDevices[i]->Release();
        }
 
        delete[] m_ppWMPDevices;
        m_ppWMPDevices = NULL;        
    }
}
```



## <a name="devices-are-displayed-in-a-list-box"></a>I dispositivi vengono visualizzati in una casella di riepilogo

La funzione GetSelectedDeviceIndex restituisce l'indice del dispositivo selezionato dall'utente in una casella di riepilogo usando il codice seguente:


```C++
long CMainDlg::GetSelectedDeviceIndex()
{
    return (long)SendMessage(GetDlgItem(IDC_DEVICES), LB_GETCURSEL, 0, 0);
}
```



## <a name="user-interface-state-is-managed-by-a-single-function"></a>Interfaccia utente stato è gestito da una singola funzione

La funzione SetUIState gestisce l'interfaccia utente.


```C++
SetUIState(UIState 
NewState, BOOL 
bConnected)
```



I dettagli di questa funzione non sono rilevanti per le discussioni in questa sezione, ma tenere presente che questa funzione esegue attività come l'abilitazione o la disabilitazione dei controlli e la modifica del testo visualizzato nell'interfaccia utente.

L'enumerazione UIState è stata definita come segue:


```C++
enum UIState
{
    Partnership,
    NoPartnership,
    Synchronizing
};
```



Il *parametro bConnected* specifica se configurare l'interfaccia utente per un dispositivo connesso (TRUE indica che il dispositivo è connesso). I *parametri NewState* *e bConnected* comunicano le informazioni necessarie per il funzionamento della funzione.

Le sezioni seguenti forniscono le spiegazioni del codice di esempio:

-   [Enumerazione dei dispositivi](enumerating-devices.md)
-   [Recupero degli attributi del dispositivo](retrieving-device-attributes.md)
-   [Visualizzazione dello stato di avanzamento della sincronizzazione](showing-synchronization-progress.md)
-   [Gestione delle playlist di sincronizzazione](managing-synchronization-playlists.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida al controllo del giocatore**](player-control-guide.md)
</dt> </dl>

 

 




