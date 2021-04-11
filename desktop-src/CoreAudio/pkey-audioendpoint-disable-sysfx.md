---
description: La \_ Proprietà pkey AudioEndpoint \_ Disable \_ SysFx specifica se gli effetti di sistema sono abilitati nel flusso in modalità condivisa che scorre verso o dal dispositivo dell'endpoint audio.
ms.assetid: 9e73e9b6-1864-49cb-adf8-233cc1f9bfe5
title: PKEY_AudioEndpoint_Disable_SysFx (mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61a5486222c1c22158c70864b2b9bb0c4c31b5e1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127310"
---
# <a name="pkey_audioendpoint_disable_sysfx"></a>PKEY \_ AudioEndpoint \_ Disabilita \_ SysFx

La proprietà **pkey \_ AudioEndpoint \_ Disable \_ SysFx** specifica se gli effetti di sistema sono abilitati nel flusso in modalità condivisa che scorre verso o dal dispositivo dell'endpoint audio.

Gli effetti di sistema sono implementati come oggetti di elaborazione audio (APOs) che possono essere inseriti in un flusso audio. APOs sono moduli software che eseguono funzioni di elaborazione audio quali il controllo del volume e la conversione del formato. La disabilitazione degli effetti di sistema per un dispositivo endpoint consente al flusso associato di passare attraverso il APOs non modificato.

Per ulteriori informazioni sugli effetti di sistema in Windows Vista, vedere i white paper intitolati "effettivi audio personalizzati in Windows Vista" e "riutilizzo di Windows Vista Audio System Effects" nel sito Web [tecnologie per dispositivi audio per Windows](https://www.microsoft.com/whdc/device/audio/default.mspx) .

Questa proprietà si applica solo agli effetti locali e agli effetti globali APOs installati dal file con estensione inf che ha installato la scheda audio a cui è connesso il dispositivo endpoint. Inoltre, questa proprietà influisce solo sul dispositivo endpoint di destinazione, ma non ha alcun effetto sugli effetti del sistema per altri dispositivi endpoint, anche se si connettono alla stessa scheda.

Il membro **VT** della struttura **PROPVARIANT** è impostato su **VT \_ UI4**.

Il membro **ulVal** della struttura **PROPVARIANT** è impostato su **endpoint \_ SYSFX \_ Enabled** se gli effetti di sistema sono abilitati o sull' **endpoint \_ SYSFX \_ disabilitato** se sono disabilitati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Mmdeviceapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà endpoint audio**](audio-endpoint-properties.md)
</dt> <dt>

[Proprietà audio principali](core-audio-properties.md)
</dt> </dl>

 

 




