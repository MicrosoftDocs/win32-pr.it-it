---
UID: NF:directml.IDMLDevice1.CompileGraph
title: IDMLDevice1::CompileGraph
description: Compila un grafo di operatori DirectML in un oggetto che può essere inviato alla GPU.
helpviewer_keywords:
- CompileGraph
- CompileGraph method
- CompileGraph method
- IDMLDevice1 interface
- IDMLDevice1 interface
- CompileGraph method
- IDMLDevice1.CompileGraph
- IDMLDevice1::CompileGraph
- direct3d12.idmldevice1_compileoperator
- directml/IDMLDevice1::CompileGraph
ms.topic: reference
tech.root: directml
ms.date: 11/04/2020
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: DirectML.lib
req.dll: DirectML.dll
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- IDMLDevice1::CompileGraph
- directml/IDMLDevice1::CompileGraph
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- DirectML.dll
api_name:
- IDMLDevice1.CompileGraph
ms.openlocfilehash: 8a9b4ce9bd8f8bd8b1d6f2a6bbd144009eb0d79d
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803746"
---
# <a name="idmldevice1compilegraph-method-directmlh"></a>Metodo IDMLDevice1::CompileGraph (directml.h)

Compila un grafo di operatori DirectML in un oggetto che può essere inviato alla GPU.

Un operatore compilato rappresenta la forma efficiente e cotta di un operatore adatto per l'esecuzione nella GPU. Un operatore compilato contiene lo stato (ad esempio shader e altri oggetti) necessario per l'esecuzione. Poiché un operatore compilato implementa [l'interfaccia IDMLPageable,](/windows/win32/api/directml/nn-directml-idmlpageable) se lo si desidera, è possibile evilirne uno dalla memoria GPU. Per altre informazioni, vedere [IDMLDevice1::Evict](/windows/win32/api/directml/nf-directml-idmldevice-evict) e [IDMLDevice1::MakeResident.](/windows/win32/api/directml/nf-directml-idmldevice-makeresident)

L'operatore compilato non usa né fa riferimento agli [oggetti IDMLOperator](/windows/win32/api/directml/nn-directml-idmloperator) forniti nella descrizione del grafo dopo la restituita di questo metodo.

> [!IMPORTANT]
> Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive). Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintassi

```cpp
HRESULT CompileGraph(
  const DML_GRAPH_DESC *desc,
  DML_EXECUTION_FLAGS  flags,
  REFIID               riid,
  void                 **ppv
);
```

## <a name="parameters"></a>Parametri

`desc`

Tipo: **[DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md)\***

Descrizione del grafo da compilare. Vedere [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md).

`flags`

Tipo: [ **DML_EXECUTION_FLAGS**](/windows/win32/api/directml/ne-directml-dml_execution_flags)

Flag per controllare l'esecuzione di questo operatore.

`riid`

Tipo: <b>REFIID</b>

Riferimento all'identificatore univoco globale (GUID) dell'interfaccia che si desidera restituire in <i>ppv</i>. Si prevede che sia il GUID di [IDMLCompiledOperator](/windows/win32/api/directml/nn-directml-idmlcompiledoperator).

`ppv`

Tipo: <b>void**</b>

Puntatore a un blocco di memoria che riceve un puntatore all'operatore compilato. Si tratta dell'indirizzo di un puntatore a [un oggetto IDMLCompiledOperator](/windows/win32/api/directml/nn-directml-idmlcompiledoperator)che rappresenta l'operatore compilato creato.


## <a name="return-value"></a>Valore restituito

Tipo: [ **HRESULT**](/windows/desktop/winprog/windows-data-types)

Se questo metodo ha esito positivo, restituisce **S_OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

L'API Graph dell'operatore DirectML offre un modo astratto per usare DirectML in modo efficiente in hardware eterogeneo. DirectML applica ottimizzazioni a livello di tensore, ad esempio la scelta del layout tensore più efficiente in base all'adattatore in uso. Applica anche le ottimizzazioni, ad esempio la rimozione degli operatori Join o Split.

È consigliabile applicare ottimizzazioni di alto livello prima di compilare un grafo DirectML. Ad esempio, il fusing degli operatori di convoluzione con BatchNorm, la trasformazione costante e l'eliminazione di sottoespressioni comuni. Le ottimizzazioni all'interno dell'utilità di ottimizzazione dei grafi di DirectML sono progettate per integrare queste ottimizzazioni indipendenti dal dispositivo, che in genere vengono gestite in modo generico dai framework di Machine Learning.

## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Piattaforma di destinazione** | Windows |
| **Intestazione** | directml.h |
| **Libreria** | DirectML.lib |
| **DLL** | DirectML.dll |

## <a name="see-also"></a>Vedi anche

[IDMLDevice1](/windows/win32/api/directml/nn-directml-idmldevice)