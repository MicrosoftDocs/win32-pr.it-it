---
title: IDXCoreAdapterFactory::CreateAdapterList
description: Genera un elenco di oggetti adapter che rappresentano lo stato corrente dell'adattatore del sistema e soddisfano i criteri specificati.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 0d00cba3236bf63a1691473098b1f94438b790a93a75215e36690745ee7977fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119842521"
---
# <a name="idxcoreadapterfactorycreateadapterlist-method"></a>Metodo IDXCoreAdapterFactory::CreateAdapterList

Genera un elenco di oggetti adapter che rappresentano lo stato corrente dell'adattatore del sistema e soddisfano i criteri specificati. Per indicazioni sulla programmazione ed esempi di codice, vedere [Uso di DXCore per enumerare gli adattatori.](../dxcore-enum-adapters.md)

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

Numero di elementi nella matrice a cui punta *l'argomento filterAttributes.*

### <a name="filterattributes-in"></a>filterAttributes [in]

Tipo: **CONST \* GUID**

Puntatore a una matrice di GUID dell'attributo dell'adattatore. Per un elenco di GUID di attributo, vedere GUID degli attributi [dell'adapter DXCore.](../dxcore-adapter-attribute-guids.md) È necessario specificare almeno un GUID. Nel caso in cui nella matrice siano specificati più GUID, nell'elenco restituito verranno inclusi solo gli adattatori che soddisfano tutti gli attributi richiesti. 

### <a name="riid"></a>Riid

Tipo: **REFIID**

Riferimento all'identificatore univoco globale (GUID) dell'interfaccia che si vuole restituire in *ppvAdapterList*. Si tratta dell'identificatore di interfaccia (IID) di [IDXCoreAdapterList.](./nn-dxcore_interface-idxcoreadapterlist.md)

### <a name="ppvadapterlist-out"></a>ppvAdapterList [out]

Tipo: **\* \* void**

Indirizzo di un puntatore a un'interfaccia con l'IID specificato nel *parametro riid.* Al completamento della restituzione, *\* ppvAdapterList* (l'indirizzo dereferenziato) contiene un puntatore all'elenco di adapter creato.

## <a name="returns"></a>Restituisce

Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Se la funzione ha esito positivo, restituisce **S_OK**. In caso contrario, restituisce un [**codice di errore HRESULT**](../../com/structure-of-com-error-codes.md) [](../../com/com-error-codes-10.md).

|Valore restituito|Descrizione|
|-|-|
|E_INVALIDARG|`nullptr`è stato fornito *per filterAttributes* oppure per numAttributes è stato specificato *0.*|
|E_NOINTERFACE|È stato specificato un valore non valido per *riid*.|
|E_POINTER|`nullptr` è stato fornito per *ppvAdapterList*.|

## <a name="remarks"></a>Commenti

Anche se non vengono trovati adattatori, purché gli argomenti siano **validi,** **CreateAdapterList** crea un oggetto [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) valido e restituisce S_OK . Una volta generati, gli adapter in questo elenco specifico non cambieranno. L'elenco verrà tuttavia considerato non obsoleto se una delle schede diventa in seguito non valida o se arriva un nuovo adapter che soddisfa i criteri di filtro specificati. L'elenco restituito da **CreateAdapterList** non è ordinato in alcun modo particolare, ma l'ordinamento di un elenco è coerente tra più chiamate e anche tra riavvii del sistema operativo. L'ordinamento può cambiare in caso di modifiche alla configurazione del sistema, inclusa l'aggiunta o la rimozione di una scheda o un aggiornamento del driver in una scheda esistente. È possibile registrarsi per queste modifiche [con IDXCoreAdapterFactory::RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md) usando il tipo di notifica **DXCoreNotificationType.AdapterListStale.**

## <a name="see-also"></a>Vedi anche

[IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md), [Riferimento DXCore](../dxcore-reference.md), GUID degli attributi dell'adapter [DXCore](../dxcore-adapter-attribute-guids.md), [Uso di DXCore per enumerare gli adattatori](../dxcore-enum-adapters.md)