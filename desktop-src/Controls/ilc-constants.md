---
title: Flag di creazione dell'elenco immagini (Shlobj. h)
description: Set di flag di bit che specifica il tipo di elenco di immagini da creare. Questo parametro può essere una combinazione dei valori seguenti, ma può includere solo uno dei valori di colore ILC \_ . Usato da ImageList \_ create e IImageList2 Initialize.
ms.assetid: DFEB1934-DB7F-4151-97F9-DDB2BCCC782A
topic_type:
- apiref
api_name:
- ILC_MASK
- ILC_COLOR
- ILC_COLORDDB
- ILC_COLOR4
- ILC_COLOR8
- ILC_COLOR16
- ILC_COLOR24
- ILC_COLOR32
- ILC_PALETTE
- ILC_MIRROR
- ILC_PERITEMMIRROR
- ILC_ORIGINALSIZE
- ILC_HIGHQUALITYSCALE
api_location:
- Shlobj.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f27f9a83c119b8e201ba41c002bf7c166ba3e4dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476318"
---
# <a name="image-list-creation-flags"></a>Flag di creazione dell'elenco immagini

Set di flag di bit che specifica il tipo di elenco di immagini da creare. Questo parametro può essere una combinazione dei valori seguenti, ma può includere solo uno dei valori di colore ILC \_ . Usato da [**ImageList \_ create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) e [**IImageList2:: Initialize**](/windows/desktop/api/Commoncontrols/nf-commoncontrols-iimagelist2-initialize).



| Costante/valore                                                                                                                                                                                                                                     | Descrizione                                                                                                                                                                                  |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ILC_MASK"></span><span id="ilc_mask"></span><dl> <dt>**ILC \_ MASCHERA**</dt> <dt>0x00000001</dt> </dl>                                     | Usare una maschera. L'elenco di immagini contiene due bitmap, una delle quali è una bitmap monocromatica utilizzata come maschera. Se questo valore non è incluso, l'elenco di immagini contiene una sola bitmap.<br/>      |
| <span id="ILC_COLOR"></span><span id="ilc_color"></span><dl> <dt>**ILC \_**</dt> <dt>0x00000000</dt> colore </dl>                                  | Usare il comportamento predefinito se nessuno degli altri \_ flag COLORx di ILC è specificato. In genere, il valore predefinito è ILC \_ COLOR4, ma per i driver di visualizzazione precedenti, il valore predefinito è ILC \_ COLORDDB.<br/> |
| <span id="ILC_COLORDDB"></span><span id="ilc_colorddb"></span><dl> <dt>**ILC \_**</dt> <dt>0x000000FE</dt> COLORDDB </dl>                         | Usare una bitmap dipendente dal dispositivo.<br/>                                                                                                                                                    |
| <span id="ILC_COLOR4"></span><span id="ilc_color4"></span><dl> <dt>**ILC \_**</dt> <dt>0x00000004</dt> COLOR4 </dl>                               | Usare una sezione bitmap (DIB) a 4 bit (a 16 colori) come bitmap per l'elenco di immagini.<br/>                                                                                  |
| <span id="ILC_COLOR8"></span><span id="ilc_color8"></span><dl> <dt>**ILC \_**</dt> <dt>0x00000008</dt> COLOR8 </dl>                               | Usare una sezione DIB a 8 bit. I colori utilizzati per la tabella dei colori sono uguali a quelli della tavolozza dei mezzitoni.<br/>                                                                        |
| <span id="ILC_COLOR16"></span><span id="ilc_color16"></span><dl> <dt>**ILC \_**</dt> <dt>0x00000010</dt> COLOR16 </dl>                            | Usare una sezione DIB a 16 bit (32/64K-Color).<br/>                                                                                                                                          |
| <span id="ILC_COLOR24"></span><span id="ilc_color24"></span><dl> <dt>**ILC \_**</dt> <dt>0x00000018</dt> COLOR24 </dl>                            | Usare una sezione DIB a 24 bit.<br/>                                                                                                                                                         |
| <span id="ILC_COLOR32"></span><span id="ilc_color32"></span><dl> <dt>**ILC \_**</dt> <dt>0x00000020</dt> COLOR32 </dl>                            | Usare una sezione DIB a 32 bit.<br/>                                                                                                                                                         |
| <span id="ILC_PALETTE"></span><span id="ilc_palette"></span><dl> <dt>**ILC \_ TAVOLOzza**</dt> <dt>0x00000800</dt> </dl>                            | Non implementato.<br/>                                                                                                                                                                  |
| <span id="ILC_MIRROR"></span><span id="ilc_mirror"></span><dl> <dt>**ILC \_**</dt> <dt>0x00002000</dt> mirror </dl>                               | Specchia le icone contenute, se il processo è con mirroring<br/>                                                                                                                            |
| <span id="ILC_PERITEMMIRROR"></span><span id="ilc_peritemmirror"></span><dl> <dt>**ILC \_**</dt> <dt>0x00008000</dt> PERITEMMIRROR </dl>          | Fa in modo che il codice di mirroring rispecchi ogni elemento quando si inserisce un set di immagini, rispetto all'intera striscia.<br/>                                                                             |
| <span id="ILC_ORIGINALSIZE"></span><span id="ilc_originalsize"></span><dl> <dt>**ILC \_**</dt> <dt>0x00010000</dt> ORIGINALSIZE </dl>             | **Windows Vista e versioni successive.** ImageList deve accettare le immagini di set minori di e applicare le dimensioni originali in base all'immagine aggiunta.<br/>                                                        |
| <span id="ILC_HIGHQUALITYSCALE"></span><span id="ilc_highqualityscale"></span><dl> <dt>**ILC \_**</dt> <dt>0x00020000</dt> HIGHQUALITYSCALE </dl> | **Windows Vista e versioni successive.** Riservato.<br/>                                                                                                                                            |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                      |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 





