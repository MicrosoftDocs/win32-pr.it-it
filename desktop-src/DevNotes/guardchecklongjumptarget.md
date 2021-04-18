---
UID: ''
title: GuardCheckLongJumpTarget (funzione)
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
ms.openlocfilehash: 02f659f77ab2bace129c9b9d9011b4c93e59b2f4
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/11/2020
ms.locfileid: "106299550"
---
# <a name="guardchecklongjumptarget-function"></a>GuardCheckLongJumpTarget (funzione)

## <a name="description"></a>Descrizione

Tenta di verificare se la destinazione di un [longjmp](/cpp/c-runtime-library/reference/longjmp) è valida per un processo con [protezione del flusso di controllo (cfg)](../secbp/control-flow-guard.md) abilitata.

Se l'indirizzo di destinazione corrisponde a un mapping di immagini, vengono estratte le destinazioni valide per il file binario.
La funzione utilizza tali destinazioni per convalidare la destinazione.
Se il file binario non contiene metadati che descrivono il set di destinazioni *longjmp* valide, la funzione restituisce **true**.

Se l'indirizzo di destinazione corrisponde a un mapping non di immagine, come nel codice JIT, viene consultato un criterio globale di sola lettura per determinare se il salto è consentito.

## <a name="parameters"></a>Parametri

### <a name="targetaddress-in"></a>TargetAddress [in]

Indirizzo di destinazione per il salto.

### <a name="flags-in"></a>Flags [in]

Flag che descrivono l'operazione da eseguire sull'indirizzo.
Se si specifica **GUARD_CHECK_LONGJUMP_NON_FATAL** (0x1), questa funzione non termina il processo se la destinazione non è valida.

## <a name="returns"></a>Restituisce

**True** se la destinazione è valida; in caso contrario, **false**.

## <a name="remarks"></a>Commenti

## <a name="see-also"></a>Vedere anche
