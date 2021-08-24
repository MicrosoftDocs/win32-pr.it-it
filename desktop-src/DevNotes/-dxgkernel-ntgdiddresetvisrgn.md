---
description: Usato per consentire alla modalità utente di acquisire una conoscenza valida dell'area di ritaglio per le finestre sul desktop. Questo ritaglio può cambiare in modo asincrono dal punto di vista dei thread in modalità utente.
ms.assetid: 286f1c06-c27b-42bd-aecc-3a6923e3df29
title: Funzione NtGdiDdResetVisrgn (Ntgdi.h)
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
ms.openlocfilehash: 3077351b804f854520cff421fcad8a575278bb5a960f60ef760db38e7ca2f3a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119833641"
---
# <a name="ntgdiddresetvisrgn-function"></a>Funzione NtGdiDdResetVisrgn

\[Questa funzione è soggetta a modifiche con ogni revisione del sistema operativo. Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs. Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà nell'interazione diretta con i driver di visualizzazione.\]

Usato per consentire alla modalità utente di acquisire una conoscenza valida dell'area di ritaglio per le finestre sul desktop. Questo ritaglio può cambiare in modo asincrono dal punto di vista dei thread in modalità utente.

## <a name="syntax"></a>Sintassi


```C++
BOOL APIENTRY NtGdiDdResetVisrgn(
  _In_ HANDLE hSurface,
  _In_ HWND   hwnd
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hSurface* \[ Pollici\]
</dt> <dd>

Puntatore all'oggetto in modalità utente di qualsiasi superficie appartenente al dispositivo DirectDraw per cui deve essere reimpostato il ritaglio. Per informazioni dettagliate, vedere la documentazione di DDK.

</dd> <dt>

*hwnd* \[ Pollici\]
</dt> <dd>

Riservato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se ha esito positivo, questa funzione restituisce **TRUE;** In caso contrario, **restituisce FALSE.**

## <a name="remarks"></a>Commenti

Il ritaglio può cambiare in modo asincrono dal punto di vista dei thread in modalità utente. Le parti in modalità kernel di DirectDraw e Windows Graphics Device Interface (GDI) mantengono un contatore che viene incrementato ogni volta che viene modificato l'elenco di ritaglio per l'intero desktop. Una chiamata a questa funzione registra questo contatore con ogni superficie primaria DirectDraw esistente nel sistema.

In un secondo momento, quando una di queste superfici primarie viene modificata da un'operazione [IDirectDrawSurface7::Blt](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-blt) o [IDirectDrawSurface7::Lock](/previous-versions/ms858221(v=msdn.10)) (vedere la documentazione di DDK), il contatore registrato con la superficie viene confrontato con il contatore globale. Se questi valori sono diversi, viene restituito un codice di errore DDERR \_ VISRGNCHANGED al codice in modalità utente. Il codice in modalità utente esegue quindi una nuova query sul ritaglio corrente per il desktop, chiama **NtGdiDdResetVisrgn** e prova di nuovo IDirectDrawSurface7::Blt applicato alla superficie primaria, rispettando il nuovo ritaglio. Alla fine, il ritaglio campionato dal codice in modalità utente sarà uguale al ritaglio corrente di proprietà della modalità kernel e IDirectDrawSurface7::Blt sarà autorizzato a continuare.

È consigliabile che le applicazioni usino l'interfaccia [IDirectDrawClipper](/previous-versions/aa919448(v=msdn.10)) o il metodo [IDirect3DDevice8::P resent](/previous-versions/ms889707(v=msdn.10)) per gestire le modifiche di ritaglio asincrone. Questi costrutti implementano il ritaglio asincrono in modo automatizzato e indipendente dal sistema operativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Ntgdi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Supporto client di basso livello per grafica](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[**DdResetVisrgn**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddresetvisrgn)
</dt> </dl>

 

 
