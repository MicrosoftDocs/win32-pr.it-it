---
UID: ''
title: Funzione GuardCheckLongJumpTarget
description: Tenta di verificare se la destinazione di un longjmp è valida.
old-location: ''
ms.assetid: na
ms.date: 04/02/2019
ms.keywords: ''
ms.topic: reference
req.header: guardapiset.h
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
req.lib: ''
req.dll: ''
req.irql: ''
topic_type:
- APIRef
api_type:
- DllExport
api_location:
- api-ms-win-core-guard-l1-1-0.dll
api_name:
- GuardCheckLongJumpTarget
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: bcc8565401e09e8a4a3e0dfb221f240255b00bd0e91b9c2611b21db3ee1c0201
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002261"
---
# <a name="guardchecklongjumptarget-function"></a>Funzione GuardCheckLongJumpTarget

## <a name="description"></a>Descrizione

Tenta di verificare se la destinazione di [un longjmp](/cpp/c-runtime-library/reference/longjmp) è valida per un processo con [Control Flow Guard (CFG)](../secbp/control-flow-guard.md) abilitato.

Se l'indirizzo di destinazione corrisponde a un mapping di immagini, le destinazioni valide vengono estratte per il file binario.
La funzione usa tali destinazioni per convalidare la destinazione.
Se il file binario non dispone di metadati che descrivono il set di *destinazioni longjmp* valide, la funzione restituisce **TRUE.**

Se l'indirizzo di destinazione corrisponde a un mapping non di immagine, come nel codice JIT, viene consultato un criterio di sola lettura globale per determinare se il passaggio è consentito.

## <a name="parameters"></a>Parametri

### <a name="targetaddress-in"></a>TargetAddress [in]

Indirizzo di destinazione per il salto.

### <a name="flags-in"></a>Flags [in]

Flag che descrivono l'operazione da eseguire sull'indirizzo.
Se si specifica **GUARD_CHECK_LONGJUMP_NON_FATAL** (0x1), questa funzione non termina il processo se la destinazione non è valida.

## <a name="returns"></a>Restituisce

**TRUE** se la destinazione è valida; in caso **contrario, FALSE.**

## <a name="remarks"></a>Commenti

## <a name="see-also"></a>Vedere anche
