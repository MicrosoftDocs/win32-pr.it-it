---
UID: ''
title: LsaManageSidNameMapping (funzione)
description: Aggiunge o rimuove i mapping SID/nome dal set di mapping registrato con il servizio di ricerca LSA.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: ''
ms.topic: reference
req.header: Ntsecapi.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Secur32.lib
req.dll:
- Advapi32.dll
- API-MS-Win-DownLevel-AdvAPI32-l4-1-0.dll
- API-MS-Win-security-lsalookup-l2-1-1.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location: ''
api_name:
- LsaManageSidNameMapping
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: fc0065c3964718d690149693f3c71ec4e9f676ec
ms.sourcegitcommit: 382c7259008374408368c173e0027fb641c848fe
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/22/2020
ms.locfileid: "104336618"
---
# <a name="lsamanagesidnamemapping-function"></a>LsaManageSidNameMapping (funzione)

## <a name="description"></a>Descrizione

La funzione **LsaManageSidNameMapping** aggiunge o rimuove i mapping SID/Name dal set di mapping registrato con il servizio di ricerca LSA.

```cpp
void WINAPI LsaManageSidNameMapping(
  _In_  LSA_SID_NAME_MAPPING_OPERATION_TYPE    OpType,
  _In_  PLSA_SID_NAME_MAPPING_OPERATION_INPUT  OpInput,
  _Out_ PLSA_SID_NAME_MAPPING_OPERATION_OUTPUT *OpOutput
);
```

## <a name="parameters"></a>Parametri

### <a name="optype-in"></a>OpType [in]

Indica se è in corso la chiamata di questa funzione per aggiungere o rimuovere un mapping SID/Name.

### <a name="opinput-in"></a>OpInput [in]

Indica i valori di dominio, account e SID da utilizzare durante l'operazione. È anche possibile impostare flag aggiuntivi all'interno di questa struttura.

### <a name="opoutput-out"></a>OpOutput [out]

Contiene un valore di [LSA_SID_NAME_MAPPING_OPERATION_ERROR](/previous-versions/windows/desktop/legacy/dn280707(v=vs.85)) che indica l'esito positivo o negativo dell'operazione.

| Valore | Significato |
|-------|---------|
| **Success** | L'operazione è stata completata senza errori. |
| **NonMappingError** | Si è verificato un errore non correlato al mapping del nome SID. |
| **NameCollision** | Operazione non riuscita a causa di un conflitto di nomi. |
| **SidCollision** | Operazione non riuscita a causa di un conflitto SID. |
| **DomainNotFound** | Dominio corrispondente non trovato. |
| **DomainSidPrefixMismatch** | Il prefisso di dominio del SID specificato non è corretto. |
| **MappingNotFound** | Il mapping non è stato trovato nella cache. |

## <a name="returns"></a>Restituisce

Se il mapping viene inserito correttamente, il valore restituito viene STATUS_SUCCESS.
In caso contrario, se la funzione ha esito negativo a causa di conflitti di nome o SID, viene restituito STATUS_INVALID_PARAMETER errore.

## <a name="remarks"></a>Commenti

## <a name="see-also"></a>Vedere anche
