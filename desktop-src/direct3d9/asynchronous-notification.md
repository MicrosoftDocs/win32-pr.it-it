---
description: Sono disponibili numerose query interessanti su un driver che un'applicazione può eseguire se non si verifica alcun costo in termini di prestazioni.
ms.assetid: 81e1c5c5-03bc-4598-814e-14e56513e221
title: Notifica asincrona (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8aee8acb791e2e1e2de7eb305cc19df4e7711e2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304882"
---
# <a name="asynchronous-notification-direct3d-9"></a>Notifica asincrona (Direct3D 9)

Sono disponibili numerose query interessanti su un driver che un'applicazione può eseguire se non si verifica alcun costo in termini di prestazioni. In Direct3D 7 e Direct3D 8, un meccanismo di query sincrono, GetInfo, funziona bene per elementi come le statistiche, ma non sono state aggiunte query critiche per le prestazioni. Sono presenti altri elementi, come le barriere, intrinsecamente asincroni. Si tratta di un'API semplice per eseguire query sia sincrone che asincrone. GetInfo verrà ritirato in Direct3D 9.

Creare una query usando [**IDirect3DDevice9:: CreateQuery**](/windows/desktop/api). Questo metodo accetta D3DQUERYTYPE, che definisce il tipo di query da creare e restituisce un puntatore a un oggetto [**IDirect3DQuery9**](/windows/desktop/api) . Se il tipo di query non è supportato, la chiamata restituisce un errore D3DERR \_ NOTAVAILABLE. Utilizzando l'oggetto query, l'applicazione invia la query al runtime utilizzando [**IDirect3DQuery9:: Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue)ed esegue il polling dello stato della query utilizzando [**IDirect3DQuery9:: GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata). Se il risultato della query è disponibile, viene \_ restituito s OK. in caso contrario, \_ viene restituito s false. Si prevede che l'applicazione passi un buffer di dimensioni appropriate per i risultati della query.

L'applicazione ha un'opzione che consente di forzare il runtime a scaricare la query fino al driver usando D3DGETDATA \_ Flush con [**IDirect3DQuery9:: GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata). Causa uno scaricamento, forzando il driver a visualizzare la query. In questo caso, \_ viene restituito D3DERR DEVICELOST se il dispositivo viene perso.

Tutte le query vengono perse quando il dispositivo viene perso, l'applicazione deve crearle nuovamente. Se il dispositivo non supporta la query e pQueryID è **null**, la creazione della query avrà esito negativo con D3DERR \_ INVALIDCALL.

Nella tabella seguente vengono riepilogate informazioni importanti su ogni tipo di query.



| QuertyType                    | Flag di problema valido              | Buffer GetData              | Runtime      | Inizio implicito della query |
|-------------------------------|-------------------------------|-----------------------------|--------------|-----------------------------|
| \_VCACHE D3DQUERYTYPE          | \_Fine D3DISSUE                 | \_VCACHE D3DDEVINFO          | Vendita al dettaglio/debug | CreateDevice                |
| \_RESOURCEMANAGER D3DQUERYTYPE | \_Fine D3DISSUE                 | \_RESOURCEMANAGER D3DDEVINFO | Solo debug   | Presente                     |
| \_VERTEXSTATS D3DQUERYTYPE     | \_Fine D3DISSUE                 | \_D3DVERTEXSTATS D3DDEVINFO  | Solo debug   | Presente                     |
| \_Evento D3DQUERYTYPE           | \_Fine D3DISSUE                 | BOOL                        | Vendita al dettaglio/debug | CreateDevice                |
| \_Occlusione D3DQUERYTYPE       | D3DISSUE \_ Begin, D3DISSUE \_ end | DWORD                       | Vendita al dettaglio/debug | N/D                         |



 

Campo Flags per [**IDirect3DQuery9:: Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue):


```
#define D3DISSUE_END (1 << 0) 
// Tells the runtime to issue the end of a query, changing its state to 
//   "non-signaled" 
```




```
 
#define D3DISSUE_BEGIN (1 << 1) // Tells the runtime to issue the 
// beginning of a query. 
```



Campo Flags per [**IDirect3DQuery9:: GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata):


```
 
#define D3DGETDATA_FLUSH (1 << 0) // Tells the runtime to flush 
// if the query is outstanding.
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Suggerimenti per la programmazione](programming-tips.md)
</dt> </dl>

 

 
