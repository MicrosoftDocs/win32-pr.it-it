---
description: Specifica informazioni sul segnale video, diverse dal livello di protezione.
ms.assetid: ed78b7eb-bf15-4068-ab86-ae42a5e62096
title: OPM_SET_ACP_AND_CGMSA_SIGNALING (Opmapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 265d2986c624e30d342a4b3bc5e957e04c56bd01d51e146536de5731db42ace8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119343511"
---
# <a name="opm_set_acp_and_cgmsa_signaling"></a>OPM \_ SET \_ ACP \_ AND \_ CGMSA \_ SIGNALING

Specifica informazioni sul segnale video, diverse dal livello di protezione.



| Requisito | Valore |
|--------------|---------------------------------------------------------------------------------------------------------------------|
| GUID del comando | OPM \_ SET \_ ACP \_ AND \_ CGMSA \_ SIGNALING                                                                                |
| Dati di input   | Struttura [**OPM \_ SET \_ ACP E \_ \_ CGMSA \_ SIGNALING \_ PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_acp_and_cgmsa_signaling_parameters) |



 

## <a name="remarks"></a>Commenti

Questo comando equivale al comando DXVA \_ COPPSetSignaling usato in Certified Output Protection Protocol (COPP).

Per CGMS-A, alcuni standard di protezione richiedono che il segnale televisivo contenga informazioni all'interno degli stessi pacchetti di forma d'onda VBI dei bit CGMS-A. Tra le altre cose, queste informazioni includono le proporzioni dell'immagine. Se le informazioni sulle proporzioni non sono coerenti con il flusso video, è possibile che i programmi televisivi non siano visualizzati in modo non coerente. L'applicazione può usare questo comando per specificare le proporzioni in modo che il driver di grafica possa generare i pacchetti VBI corretti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                      |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Opmapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)
</dt> <dt>

[Comandi OPM](opm-commands.md)
</dt> </dl>

 

 




