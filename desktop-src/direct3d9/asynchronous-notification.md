---
description: Esistono un numero di query interessanti su un driver che un'applicazione può eseguire se non sono presenti costi per le prestazioni.
ms.assetid: 81e1c5c5-03bc-4598-814e-14e56513e221
title: Notifica asincrona (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbd23a64e613bbbae56154dc35c05bcf08b75c4c91f306360153e775e12c40ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123418"
---
# <a name="asynchronous-notification-direct3d-9"></a>Notifica asincrona (Direct3D 9)

Esistono un numero di query interessanti su un driver che un'applicazione può eseguire se non sono presenti costi per le prestazioni. In Direct3D 7 e Direct3D 8, un meccanismo di query sincrono, GetInfo, funzionava bene per operazioni come le statistiche, ma non sono state aggiunte query critiche per le prestazioni. Esistono altri elementi (ad esempio recinti) intrinsecamente asincroni. Si tratta di un'API semplice per eseguire query sincrone e asincrone. GetInfo verrà ritirato in Direct3D 9.

Creare una query [**usando IDirect3DDevice9::CreateQuery**](/windows/desktop/api). Questo metodo accetta un oggetto D3DQUERYTYPE, che definisce il tipo di query da eseguire e restituisce un puntatore a [**un oggetto IDirect3DQuery9.**](/windows/desktop/api) Se il tipo di query non è supportato, la chiamata restituisce un errore D3DERR \_ NOTAVAILABLE. Usando l'oggetto query, l'applicazione invia la query al runtime usando [**IDirect3DQuery9::Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue)ed esegue il polling dello stato della query [**usando IDirect3DQuery9::GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata). Se il risultato della query è disponibile, viene restituito S \_ OK. In caso contrario, viene restituito S \_ FALSE. È previsto che l'applicazione passi un buffer di dimensioni appropriate per i risultati della query.

L'applicazione può forzare il runtime a scaricare la query nel driver usando D3DGETDATA \_ FLUSH con [**IDirect3DQuery9::GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata). Causa uno scaricamento, forzando il driver a visualizzare la query. In questo caso, viene restituito D3DERR \_ DEVICELOST se il dispositivo viene perso.

Tutte le query vengono perse quando il dispositivo viene perso e l'applicazione deve ri-crearle. Se il dispositivo non supporta la query e pQueryID è **NULL,** la creazione della query avrà esito negativo con D3DERR \_ INVALIDCALL.

Nella tabella seguente vengono riepilogate informazioni importanti su ogni tipo di query.



| QuertyType                    | Flag di problema valido              | Buffer GetData              | Runtime      | Inizio implicito della query |
|-------------------------------|-------------------------------|-----------------------------|--------------|-----------------------------|
| D3DQUERYTYPE \_ VCACHE          | D3DISSUE \_ END                 | D3DDEVINFO \_ VCACHE          | Vendita al dettaglio/debug | CreateDevice                |
| D3DQUERYTYPE \_ ResourceManager | D3DISSUE \_ END                 | D3DDEVINFO \_ ResourceManager | Solo debug   | Presente                     |
| D3DQUERYTYPE \_ VERTEXSTATS     | D3DISSUE \_ END                 | D3DDEVINFO \_ D3DVERTEXSTATS  | Solo debug   | Presente                     |
| EVENTO D3DQUERYTYPE \_           | D3DISSUE \_ END                 | BOOL                        | Vendita al dettaglio/debug | CreateDevice                |
| OCCLUSIONE D3DQUERYTYPE \_       | D3DISSUE \_ BEGIN,D3DISSUE \_ END | DWORD                       | Vendita al dettaglio/debug | N/A                         |



 

Campo Flags per [**IDirect3DQuery9::Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue):


```
#define D3DISSUE_END (1 << 0) 
// Tells the runtime to issue the end of a query, changing its state to 
//   "non-signaled" 
```




```
 
#define D3DISSUE_BEGIN (1 << 1) // Tells the runtime to issue the 
// beginning of a query. 
```



Campo Flags per [**IDirect3DQuery9::GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata):


```
 
#define D3DGETDATA_FLUSH (1 << 0) // Tells the runtime to flush 
// if the query is outstanding.
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Programmazione Suggerimenti](programming-tips.md)
</dt> </dl>

 

 
