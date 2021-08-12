---
title: IDXCoreAdapterList::Sort
description: Ordina un oggetto elenco di adattatori DXCore in base a una matrice di input fornita di criteri di ordinamento.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/03/2019
ms.openlocfilehash: 59580fb8b76c80a264796f829d2b0a1d2e8eabb4375896fbd27fb34a7697cf90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118278872"
---
# <a name="idxcoreadapterlistsort-method"></a>Metodo IDXCoreAdapterList::Sort

## <a name="description"></a>Descrizione

Ordina un oggetto elenco di adattatori DXCore in base a una matrice di input fornita di criteri di ordinamento, in cui agli elementi della matrice di criteri viene assegnato un peso maggiore. **L'ordinamento** consente di trovare più facilmente l'adattatore ideale in un elenco di adattatori.

## <a name="syntax"></a>Sintassi

```cpp
HRESULT Sort(
  uint32_t numPreferences,
  _In_reads_(numPreferences) const DXCoreAdapterPreference* preferences
);
```

## <a name="parameters"></a>Parametri

### <a name="numpreferences"></a>numPreferences

Tipo: **uint32_t**

Numero di elementi presenti nella matrice a cui punta il *parametro preferences.*

### <a name="preferences-in"></a>preferenze [in]

Tipo: **const [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) \***

Puntatore a una matrice costante di valori [DXCoreAdapterPreference,](./ne-dxcore_interface-dxcoreadapterpreference.md) che rappresenta i criteri di ordinamento.

## <a name="returns"></a>Restituisce

Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Se la funzione ha esito positivo, restituisce **S_OK**. In caso contrario, restituisce un [**codice di errore HRESULT**](../../com/structure-of-com-error-codes.md) [](../../com/com-error-codes-10.md).

|Valore restituito|Descrizione|
|-|-|
|E_INVALIDARG|*L'argomento numPreferences* è zero oppure l'argomento *preferences* è `nullptr` .|

## <a name="remarks"></a>Commenti

Nei casi in cui un valore [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) specificato non viene riconosciuto dal sistema operativo, viene ignorato e non causa l'esito negativo dell'API. I **valori noti di DXCoreAdapterPreference** verranno comunque considerati in questo caso. Per determinare se un tipo di ordinamento viene riconosciuto dall'API, chiamare [IDXCoreAdapterList::IsAdapterPreferenceSupported.](./nf-dxcore_interface-idxcoreadapterlist-isadapterpreferencesupported.md)

**I valori DXCoreAdapterPreference** che si verificano in precedenza nella matrice *preferences* fornita vengono trattati con priorità più alta. 

Per informazioni dettagliate sulla logica applicata per ogni tipo, vedere la documentazione dell'enumerazione **DXCoreAdapterPreference.** La logica interna per un tipo può svilupparsi durante lo sviluppo del sistema operativo.

Quando **l'ordinamento** viene restituito, gli elementi nell'elenco di adattatori DXCore saranno stati ordinati dalla più preferibile alla meno preferibile. Pertanto, la [chiamata a IDXCoreAdapterList::GetAdapter](./nf-dxcore_interface-idxcoreadapterlist-getadapter.md) con indice 0 recupera l'adattatore che meglio corrisponde ai tipi di preferenza di ordinamento richiesti; index 1 è la corrispondenza migliore successiva e così via.

## <a name="see-also"></a>Vedi anche

[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [Riferimento DXCore](../dxcore-reference.md), [Uso di DXCore per enumerare gli adattatori](../dxcore-enum-adapters.md)