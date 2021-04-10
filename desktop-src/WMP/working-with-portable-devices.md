---
title: Uso dei dispositivi portatili
description: Uso dei dispositivi portatili
ms.assetid: 145ede07-a23b-486b-a561-9c87a48b72a8
keywords:
- Windows Media Player, dispositivi portatili
- Modello a oggetti di Windows Media Player, dispositivi portatili
- modello a oggetti, dispositivi portatili
- Controllo ActiveX Windows Media Player, dispositivi portatili
- Controllo ActiveX, dispositivi portatili
- Controllo ActiveX Windows Media Player Mobile, dispositivi portatili
- Dispositivi portatili Windows Media Player Mobile
- dispositivi portatili, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b64c6e7047864b899a2d7dca2ba4754cc7cb5dc2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332380"
---
# <a name="working-with-portable-devices"></a>Uso dei dispositivi portatili

Questa sezione descrive come usare un controllo ActiveX di Windows Media Player remoto per lavorare con i dispositivi portatili.

Gli esempi di codice in questa sezione usano le classi Active Template Library (ATL), ad esempio **CComPtr**.

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

Il puntatore **IWMPPlayer** viene archiviato in una variabile membro.


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



## <a name="retrieving-a-device-pointer"></a>Recupero di un puntatore a dispositivo

Un puntatore a un particolare dispositivo viene recuperato tramite il relativo indice di matrice utilizzando codice simile al seguente:


```C++
CComPtr<IWMPSyncDevice> spSyncDevice(m_ppWMPDevices[lIndex]);
```



Si noti che l'indice illustrato negli esempi precedenti non è l'indice di relazione per il dispositivo. Si tratta dell'indice del dispositivo nella matrice di dispositivi personalizzata.

## <a name="cleaning-up"></a>Pulizia

Gli esempi usano la funzione seguente per liberare la memoria nell'array del dispositivo e rilasciare i puntatori di interfaccia:


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



## <a name="user-interface-state-is-managed-by-a-single-function"></a>Lo stato dell'interfaccia utente è gestito da un'unica funzione

La funzione SetUIState gestisce l'interfaccia utente.


```C++
SetUIState(UIState 
NewState, BOOL 
bConnected)
```



I dettagli di questa funzione non sono rilevanti per le discussioni in questa sezione, ma tenere presente che questa funzione esegue attività quali l'abilitazione o la disabilitazione dei controlli e la modifica del testo visualizzato nell'interfaccia utente.

L'enumerazione UIState è stata definita nel modo seguente:


```C++
enum UIState
{
    Partnership,
    NoPartnership,
    Synchronizing
};
```



Il parametro *bConnected* specifica se configurare l'interfaccia utente per un dispositivo connesso (true indica che il dispositivo è connesso). I parametri *NewState* e *bConnected* contengono le informazioni necessarie per la funzione per svolgere il proprio lavoro.

Le sezioni seguenti forniscono spiegazioni del codice di esempio:

-   [Enumerazione dei dispositivi](enumerating-devices.md)
-   [Recupero degli attributi del dispositivo](retrieving-device-attributes.md)
-   [Visualizzazione dello stato di avanzamento della sincronizzazione](showing-synchronization-progress.md)
-   [Gestione delle playlist di sincronizzazione](managing-synchronization-playlists.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida al controllo del lettore**](player-control-guide.md)
</dt> </dl>

 

 




