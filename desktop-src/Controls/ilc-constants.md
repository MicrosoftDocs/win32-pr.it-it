---
title: Flag di creazione elenco immagini (Shlobj.h)
description: Set di flag di bit che specifica il tipo di elenco di immagini da creare. Questo parametro può essere una combinazione dei valori seguenti, ma può includere solo uno dei valori ILC \_ COLOR. Usato da ImageList \_ Create e IImageList2 Initialize.
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
ms.openlocfilehash: ac1197604750e5da9248200b2dbcf37e53611d83842a401aafc3d2ded70c9179
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958690"
---
# <a name="image-list-creation-flags"></a>Flag di creazione dell'elenco immagini

Set di flag di bit che specifica il tipo di elenco di immagini da creare. Questo parametro può essere una combinazione dei valori seguenti, ma può includere solo uno dei valori ILC \_ COLOR. Usato da [**ImageList \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) e [**IImageList2::Initialize**](/windows/desktop/api/Commoncontrols/nf-commoncontrols-iimagelist2-initialize).



| Costante/valore                                                                                                                                                                                                                                     | Descrizione                                                                                                                                                                                  |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ILC_MASK"></span><span id="ilc_mask"></span><dl> <dt>**IlC \_ Maschera**</dt> <dt>0x00000001</dt> </dl>                                     | Usare una maschera. L'elenco di immagini contiene due bitmap, una delle quali è una bitmap monocromatica usata come maschera. Se questo valore non è incluso, l'elenco di immagini contiene una sola bitmap.<br/>      |
| <span id="ILC_COLOR"></span><span id="ilc_color"></span><dl> <dt>**IlC \_ Color**</dt> <dt>0x00000000</dt> </dl>                                  | Usare il comportamento predefinito se non viene specificato nessuno degli altri \_ flag COLORx ilC. In genere, il valore predefinito è ILC COLOR4, ma per i driver di visualizzazione meno recenti, il valore predefinito \_ è ILC \_ COLORDDB.<br/> |
| <span id="ILC_COLORDDB"></span><span id="ilc_colorddb"></span><dl> <dt>**IlC \_ ColorDDB**</dt> <dt>0x000000FE</dt> </dl>                         | Usare una bitmap dipendente dal dispositivo.<br/>                                                                                                                                                    |
| <span id="ILC_COLOR4"></span><span id="ilc_color4"></span><dl> <dt>**IlC \_ COLOR4**</dt> <dt>0x00000004</dt> </dl>                               | Usare una sezione DIB (Device-Independent Bitmap) a 4 bit (a 16 colori) come bitmap per l'elenco di immagini.<br/>                                                                                  |
| <span id="ILC_COLOR8"></span><span id="ilc_color8"></span><dl> <dt>**IlC \_ COLOR8**</dt> <dt>0x00000008</dt> </dl>                               | Usare una sezione DIB a 8 bit. I colori usati per la tabella dei colori sono gli stessi colori della tavolozza dei mezzitoni.<br/>                                                                        |
| <span id="ILC_COLOR16"></span><span id="ilc_color16"></span><dl> <dt>**IlC \_ COLOR16**</dt> <dt>0x00000010</dt> </dl>                            | Usare una sezione DIB a 16 bit (32/64k-color).<br/>                                                                                                                                          |
| <span id="ILC_COLOR24"></span><span id="ilc_color24"></span><dl> <dt>**IlC \_ COLOR24**</dt> <dt>0x00000018</dt> </dl>                            | Usare una sezione DIB a 24 bit.<br/>                                                                                                                                                         |
| <span id="ILC_COLOR32"></span><span id="ilc_color32"></span><dl> <dt>**IlC \_ COLOR32**</dt> <dt>0x00000020</dt> </dl>                            | Usare una sezione DIB a 32 bit.<br/>                                                                                                                                                         |
| <span id="ILC_PALETTE"></span><span id="ilc_palette"></span><dl> <dt>**IlC \_ Riquadro**</dt> <dt>0x00000800</dt> </dl>                            | Non implementato.<br/>                                                                                                                                                                  |
| <span id="ILC_MIRROR"></span><span id="ilc_mirror"></span><dl> <dt>**IlC \_ MIRROR**</dt> <dt>0x00002000</dt> </dl>                               | Rispecchiare le icone contenute, se il processo è con mirroring<br/>                                                                                                                            |
| <span id="ILC_PERITEMMIRROR"></span><span id="ilc_peritemmirror"></span><dl> <dt>**IlC \_ PERITEMMIRROR**</dt> <dt>0x00008000</dt> </dl>          | Fa sì che il codice di mirroring riflesse ogni elemento durante l'inserimento di un set di immagini rispetto all'intera striscia.<br/>                                                                             |
| <span id="ILC_ORIGINALSIZE"></span><span id="ilc_originalsize"></span><dl> <dt>**IlC \_ ORIGINALSIZE**</dt> <dt>0x00010000</dt> </dl>             | **Windows Vista e versioni successive.** Imagelist deve accettare immagini inferiori a quelle impostate e applicare le dimensioni originali in base all'immagine aggiunta.<br/>                                                        |
| <span id="ILC_HIGHQUALITYSCALE"></span><span id="ilc_highqualityscale"></span><dl> <dt>**IlC \_ HIGHQUALITYSCALE**</dt> <dt>0x00020000</dt> </dl> | **Windows Vista e versioni successive.** Riservato.<br/>                                                                                                                                            |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                      |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 





