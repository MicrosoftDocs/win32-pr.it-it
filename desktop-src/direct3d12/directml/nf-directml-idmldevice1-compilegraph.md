---
UID: NF:directml.IDMLDevice1.CompileGraph
title: IDMLDevice1::CompileGraph
description: Compila un grafico di operatori DirectML in un oggetto che può essere inviato alla GPU.
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
ms.openlocfilehash: 25dbc62fac9cd38d9728a295e336038441aee19f
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320278"
---
# <a name="idmldevice1compilegraph-method-directmlh"></a>Metodo IDMLDevice1:: CompileGraph (directml. h)

Compila un grafico di operatori DirectML in un oggetto che può essere inviato alla GPU.

Un operatore compilato rappresenta il formato efficiente e cotto di un operatore adatto per l'esecuzione nella GPU. Un operatore compilato include lo stato (ad esempio shader e altri oggetti) necessario per l'esecuzione. Poiché un operatore compilato implementa l'interfaccia [IDMLPageable](/windows/win32/api/directml/nn-directml-idmlpageable) , è possibile rimuoverne uno dalla memoria GPU, se lo si desidera. Per altre informazioni, vedere [IDMLDevice1:: Rimuovi](/windows/win32/api/directml/nf-directml-idmldevice-evict) e [IDMLDevice1:: MakeResident](/windows/win32/api/directml/nf-directml-idmldevice-makeresident) .

L'operatore compilato non usa né fa riferimento agli oggetti [IDMLOperator](/windows/win32/api/directml/nn-directml-idmloperator) forniti all'interno della descrizione del grafo dopo la restituzione di questo metodo.

> [!IMPORTANT]
> Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Vedere anche [cronologia delle versioni di DirectML](../dml-version-history.md).

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

Tutti i flag per controllare l'esecuzione di questo operatore.

`riid`

Tipo: <b>REFIID</b>

Riferimento all'identificatore univoco globale (GUID) dell'interfaccia che si desidera restituire in <i>PPV</i>. Questo dovrebbe essere il GUID di [IDMLCompiledOperator](/windows/win32/api/directml/nn-directml-idmlcompiledoperator).

`ppv`

Tipo: <b>void * *</b>

Puntatore a un blocco di memoria che riceve un puntatore all'operatore compilato. Si tratta dell'indirizzo di un puntatore a un [IDMLCompiledOperator](/windows/win32/api/directml/nn-directml-idmlcompiledoperator), che rappresenta l'operatore compilato creato.


## <a name="return-value"></a>Valore restituito

Tipo: [ **HRESULT**](/windows/desktop/winprog/windows-data-types)

Se questo metodo ha esito positivo, restituisce **S_OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

L'API Graph di DirectML operator fornisce un metodo astratto per usare DirectML in modo efficiente tra diversi componenti hardware. DirectML applica le ottimizzazioni a livello di tensore, ad esempio la scelta del layout tensore più efficiente in base alla scheda utilizzata. Applica anche le ottimizzazioni, ad esempio la rimozione di operatori join o Split.

È consigliabile applicare ottimizzazioni di alto livello prima di creare un grafico DirectML. Ad esempio, fondendo gli operatori di convoluzione con BatchNorm, la riduzione costante e l'eliminazione di sottoespressioni comuni. Le ottimizzazioni all'interno dell'utilità di ottimizzazione dei grafici di DirectML sono progettate per completare queste ottimizzazioni indipendenti dal dispositivo, che in genere vengono gestite in modo generico dai framework di machine learning.

## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Piattaforma di destinazione** | Windows |
| **Intestazione** | directml. h |
| **Libreria** | DirectML. lib |
| **DLL** | DirectML.dll |

## <a name="see-also"></a>Vedi anche

[IDMLDevice1](/windows/win32/api/directml/nn-directml-idmldevice)