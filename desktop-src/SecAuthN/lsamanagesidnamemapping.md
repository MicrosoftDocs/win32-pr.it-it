---
UID: ''
title: Funzione LsaManageSidNameMapping
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
ms.openlocfilehash: 6c2a66a318076588b725f74e9f03a23b8a134595b196dbf140850e72a7d78d8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118921860"
---
# <a name="lsamanagesidnamemapping-function"></a>Funzione LsaManageSidNameMapping

## <a name="description"></a>Descrizione

La **funzione LsaManageSidNameMapping** aggiunge o rimuove i mapping SID/nome dal set di mapping registrato con il servizio di ricerca LSA.

```cpp
void WINAPI LsaManageSidNameMapping(
  _In_  LSA_SID_NAME_MAPPING_OPERATION_TYPE    OpType,
  _In_  PLSA_SID_NAME_MAPPING_OPERATION_INPUT  OpInput,
  _Out_ PLSA_SID_NAME_MAPPING_OPERATION_OUTPUT *OpOutput
);
```

## <a name="parameters"></a>Parametri

### <a name="optype-in"></a>OpType [in]

Indica se viene chiamata questa funzione per aggiungere o rimuovere un MAPPING SID/nome.

### <a name="opinput-in"></a>OpInput [in]

Indica i valori di dominio, account e SID da usare durante questa operazione. All'interno di questa struttura è anche possibile impostare flag aggiuntivi.

### <a name="opoutput-out"></a>OpOutput [out]

Contiene un valore [di](/previous-versions/windows/desktop/legacy/dn280707(v=vs.85)) LSA_SID_NAME_MAPPING_OPERATION_ERROR che indica l'esito positivo o negativo dell'operazione.

| Valore | Significato |
|-------|---------|
| **Success** | L'operazione è stata completata senza errori. |
| **NonMappingError** | Si è verificato un errore non correlato al mapping del nome SID. |
| **NameCollision** | Errore dell'operazione a causa di un conflitto di nomi. |
| **SidCollision** | Errore dell'operazione a causa di un conflitto di SID. |
| **DomainNotFound** | Dominio corrispondente non trovato. |
| **DomainSidPrefixMismatch** | Il SID specificato non ha il prefisso di dominio corretto. |
| **MappingNotFound** | Mapping non trovato nella cache. |

## <a name="returns"></a>Restituisce

Se il mapping viene inserito correttamente, il valore restituito viene STATUS_SUCCESS.
In caso contrario, se la funzione ha esito negativo a causa di siD o conflitti di nome, STATUS_INVALID_PARAMETER verrà restituito un errore.

## <a name="remarks"></a>Commenti

## <a name="see-also"></a>Vedere anche
