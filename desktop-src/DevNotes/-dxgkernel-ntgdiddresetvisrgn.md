---
description: Consente di abilitare la modalità utente per ottenere una conoscenza valida dell'area di visualizzazione per Windows sul desktop. Questo ritaglio può variare in modo asincrono dal punto di vista dei thread in modalità utente.
ms.assetid: 286f1c06-c27b-42bd-aecc-3a6923e3df29
title: Funzione NtGdiDdResetVisrgn (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdResetVisrgn
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: dd83bcfd6c1f3dec31fb80cf78750bfdfef5e7a9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877257"
---
# <a name="ntgdiddresetvisrgn-function"></a>NtGdiDdResetVisrgn (funzione)

\[Questa funzione è soggetta a modifiche a ogni revisione del sistema operativo. Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs; Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà legate all'interazione diretta con i driver di visualizzazione.\]

Consente di abilitare la modalità utente per ottenere una conoscenza valida dell'area di visualizzazione per Windows sul desktop. Questo ritaglio può variare in modo asincrono dal punto di vista dei thread in modalità utente.

## <a name="syntax"></a>Sintassi


```C++
BOOL APIENTRY NtGdiDdResetVisrgn(
  _In_ HANDLE hSurface,
  _In_ HWND   hwnd
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hSurface* \[ in\]
</dt> <dd>

Puntatore all'oggetto in modalità utente di qualsiasi superficie appartenente al dispositivo DirectDraw per il quale deve essere reimpostato il ritaglio. Per informazioni dettagliate, vedere la documentazione di DDK.

</dd> <dt>

*HWND* \[ in\]
</dt> <dd>

Riservato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'esito è positivo, la funzione restituisce **true**. in caso contrario, restituisce **false**.

## <a name="remarks"></a>Commenti

Il ritaglio può variare in modo asincrono dal punto di vista dei thread in modalità utente. Le parti in modalità kernel di DirectDraw e Windows Graphics Device Interface (GDI) mantengono un contatore incrementato ogni volta che viene modificato l'elenco di ritaglio per l'intero desktop. Una chiamata a questa funzione registra questo contatore con ogni superficie primaria DirectDraw esistente nel sistema.

In un secondo momento, quando una di queste superfici primarie viene modificata da un'operazione [IDirectDrawSurface7:: BLT](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-blt) o [IDirectDrawSurface7:: Lock](/previous-versions/ms858221(v=msdn.10)) (vedere la documentazione di DDK), il contatore registrato con la superficie viene confrontato con il contatore globale. Se questi valori sono diversi, viene restituito un codice \_ di errore DDERR VISRGNCHANGED al codice in modalità utente. Il codice in modalità utente eseguirà nuovamente una query sul ritaglio corrente per il desktop, chiamerà **NtGdiDdResetVisrgn** e riproverà a eseguire IDirectDrawSurface7:: BLT applicato all'area primaria, rispettando il nuovo ritaglio. Infine, il ritaglio che è stato campionato dal codice in modalità utente sarà uguale al ritaglio corrente di proprietà della modalità kernel e IDirectDrawSurface7:: BLT potrà continuare.

Si consiglia di usare l'interfaccia [IDirectDrawClipper](/previous-versions/aa919448(v=msdn.10)) o [IDirect3DDevice8::P](/previous-versions/ms889707(v=msdn.10)) metodo reinviato per gestire le modifiche di ritaglio asincrono. Questi costrutti implementano il ritaglio asincrono in modo automatico e indipendente dal sistema operativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Ntgdi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Supporto client di livello inferiore grafica](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[**DdResetVisrgn**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddresetvisrgn)
</dt> </dl>

 

 
