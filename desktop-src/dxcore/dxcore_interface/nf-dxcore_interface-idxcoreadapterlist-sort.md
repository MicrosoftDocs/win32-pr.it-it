---
title: IDXCoreAdapterList::Sort
description: Ordina un oggetto elenco di adapter DXCore basato su una matrice di input fornita di criteri di ordinamento.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/03/2019
ms.openlocfilehash: 6260e700053a99b531a66a5c19e15d4a32f07e46
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118306"
---
# <a name="idxcoreadapterlistsort-method"></a>Metodo IDXCoreAdapterList:: Sort

## <a name="description"></a>Descrizione

Ordina un oggetto elenco di adapter DXCore in base a una matrice di input fornita di criteri di ordinamento, in cui gli elementi della matrice in precedenza nella matrice di criteri hanno un peso maggiore. **Ordina** consente di trovare più facilmente la scheda ideale in un elenco di adapter.

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

Numero di elementi presenti nella matrice a cui punta il parametro *Preferenze* .

### <a name="preferences-in"></a>Preferenze [in]

Tipo: **const [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) \***

Puntatore a una matrice di costanti di valori [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) , che rappresenta i criteri di ordinamento.

## <a name="returns"></a>Restituisce

Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Se la funzione ha esito positivo, restituisce **S_OK**. In caso contrario, restituisce un [codice di errore](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .

|Valore restituito|Descrizione|
|-|-|
|E_INVALIDARG|L'argomento *numPreferences* è zero oppure l'argomento di *Preferenze* è `nullptr` .|

## <a name="remarks"></a>Commenti

Nei casi in cui un valore [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) specificato non è riconosciuto dal sistema operativo, viene ignorato e non comporta l'esito negativo dell'API. In questo caso, i valori **DXCoreAdapterPreference** noti verranno comunque considerati. Per determinare se un tipo di ordinamento viene riconosciuto dall'API, chiamare [IDXCoreAdapterList:: IsAdapterPreferenceSupported](./nf-dxcore_interface-idxcoreadapterlist-isadapterpreferencesupported.md).

I valori **DXCoreAdapterPreference** che si verificano in precedenza nella matrice di *Preferenze* fornita vengono trattati con priorità più elevata. 

Per informazioni dettagliate sulla logica applicata per ogni tipo, vedere la documentazione relativa all'enumerazione **DXCoreAdapterPreference** . La logica interna per un tipo può svilupparsi durante lo sviluppo del sistema operativo.

Quando l' **ordinamento** viene restituito, gli elementi nell'elenco di adapter DXCore sono stati ordinati dal più preferibile al meno preferibile. Quindi, chiamando [IDXCoreAdapterList:: GetAdapter](./nf-dxcore_interface-idxcoreadapterlist-getadapter.md) con indice 0, viene recuperata la scheda che corrisponde maggiormente ai tipi di preferenza di ordinamento richiesti. index 1 è la prossima corrispondenza migliore e così via.

## <a name="see-also"></a>Vedi anche

Guida di [riferimento](../dxcore-reference.md)a [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), DXCore, [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md)