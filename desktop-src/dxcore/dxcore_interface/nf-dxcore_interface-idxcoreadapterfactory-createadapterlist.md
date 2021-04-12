---
title: IDXCoreAdapterFactory::CreateAdapterList
description: Genera un elenco di oggetti adapter che rappresentano lo stato corrente dell'adapter del sistema e soddisfano i criteri specificati.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 0a35d4dd9a481880d66988b6ade079534d1297c1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473747"
---
# <a name="idxcoreadapterfactorycreateadapterlist-method"></a>Metodo IDXCoreAdapterFactory:: CreateAdapterList

Genera un elenco di oggetti adapter che rappresentano lo stato corrente dell'adapter del sistema e soddisfano i criteri specificati. Per istruzioni sulla programmazione ed esempi di codice, vedere [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md).

## <a name="syntax"></a>Sintassi

```cpp
virtual HRESULT STDMETHODCALLTYPE CreateAdapterList(
  uint32_t numAttributes,
  _In_reads_(numAttributes) const GUID *filterAttributes,
  REFIID riid,
  _COM_Outptr_ void **ppvAdapterList) = 0;

template<class T>
HRESULT STDMETHODCALLTYPE CreateAdapterList(
  uint32_t numAttributes,
  _In_reads_(numAttributes) const GUID *filterAttributes,
  _COM_Outptr_ T **ppvAdapterList);
```

## <a name="parameters"></a>Parametri

### <a name="numattributes"></a>numAttributes

Tipo: **uint32_t**

Numero di elementi nella matrice a cui punta l'argomento *FilterAttributes* .

### <a name="filterattributes-in"></a>filterAttributes [in]

Tipo: **GUID \* const**

Puntatore a una matrice di GUID dell'attributo dell'adattatore. Per un elenco di GUID di attributo, vedere i [GUID dell'attributo della scheda DXCore](../dxcore-adapter-attribute-guids.md). È necessario fornire almeno un GUID. Nel caso in cui sia specificato più di un GUID nella matrice, solo gli adapter che soddisfano *tutti* gli attributi richiesti verranno inclusi nell'elenco restituito.

### <a name="riid"></a>riid

Tipo: **REFIID**

Riferimento all'identificatore univoco globale (GUID) dell'interfaccia che si desidera venga restituita in *ppvAdapterList*. Questo dovrebbe essere l'identificatore di interfaccia (IID) di [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md).

### <a name="ppvadapterlist-out"></a>ppvAdapterList [out]

Tipo: **void \* \***

Indirizzo di un puntatore a un'interfaccia con l'IID specificato nel parametro *riid* . In caso di esito positivo, *\* ppvAdapterList* (l'indirizzo dereferenziato) contiene un puntatore all'elenco di adapter creato.

## <a name="returns"></a>Restituisce

Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Se la funzione ha esito positivo, restituisce **S_OK**. In caso contrario, restituisce un [codice di errore](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .

|Valore restituito|Descrizione|
|-|-|
|E_INVALIDARG|`nullptr` è stato specificato per *FilterAttributes* oppure è stato specificato 0 per *numAttributes*.|
|E_NOINTERFACE|È stato specificato un valore non valido per *riid*.|
|E_POINTER|`nullptr` fornito per *ppvAdapterList*.|

## <a name="remarks"></a>Commenti

Anche se non viene trovato alcun adapter, finché gli argomenti sono validi, **CreateAdapterList** crea un oggetto [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) valido e restituisce **S_OK**. Una volta generati, le schede in questo elenco specifico non cambiano. Tuttavia, l'elenco verrà considerato non aggiornato se una delle schede in un secondo momento diventa non valida o se arriva un nuovo adapter che soddisfa i criteri di filtro forniti. L'elenco restituito da **CreateAdapterList** non è ordinato in alcun modo specifico, ma l'ordine di un elenco è coerente tra più chiamate e anche tra i riavvii del sistema operativo. L'ordinamento può variare in base alle modifiche apportate alla configurazione del sistema, ad esempio l'aggiunta o la rimozione di un adapter o l'aggiornamento di un driver in una scheda esistente. È possibile eseguire la registrazione per queste modifiche con [IDXCoreAdapterFactory:: RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md) usando il tipo di notifica **DXCoreNotificationType. AdapterListStale**.

## <a name="see-also"></a>Vedi anche

[IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md), [riferimento a DXCore](../dxcore-reference.md), [GUID dell'attributo della scheda DXCore](../dxcore-adapter-attribute-guids.md), [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md)