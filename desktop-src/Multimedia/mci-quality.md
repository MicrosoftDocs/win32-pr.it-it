---
title: Comando MCI_QUALITY (mmsystem. h)
description: Il \_ comando di qualità MCI definisce un livello di qualità personalizzato per la compressione di dati audio, video o di immagine continua. I dispositivi digitali video riconoscono questo comando.
ms.assetid: 91ad9704-0089-4b1f-b0f6-919ab5fd84e0
keywords:
- Comando MCI_QUALITY Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_QUALITY
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 996703c1a5b7d3adec1a001af58ebc8d916301a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400222"
---
# <a name="mci_quality-command"></a>\_Comando qualità MCI

Il \_ comando di qualità MCI definisce un livello di qualità personalizzato per la compressione di dati audio, video o di immagine continua. I dispositivi digitali video riconoscono questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_QUALITY, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_QUALITY_PARMS) lpQuality
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*
</dt> <dd>

Identificatore del dispositivo MCI che deve ricevere il messaggio di comando.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

\_Test MCI notifica, MCI \_ Wait o MCI \_ . Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpQuality"></span><span id="lpquality"></span><span id="LPQUALITY"></span>*lpQuality*
</dt> <dd>

Puntatore a una [**struttura \_ \_ \_ parametri di qualità DGV di MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_quality_parmsa) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

Il nome definito per questo livello di qualità può essere utilizzato quando si imposta la qualità audio, video o ancora con i comandi [MCI \_ sefonica](mci-setaudio.md) e [MCI \_ sevideo](mci-setvideo.md) .

I flag aggiuntivi seguenti si applicano ai dispositivi digitali video:

<dl> <dt>

<span id="MCI_QUALITY_ALG"></span><span id="mci_quality_alg"></span>\_qualità MCI \_ ALG
</dt> <dd>

Il membro **lpstrAlgorithm** della struttura identificata da *lpQuality* contiene un indirizzo di un buffer contenente il nome dell'algoritmo. Questo algoritmo deve essere supportato dal driver di dispositivo e deve essere compatibile con il descrittore audio, ancora o video usato. Se questo flag viene omesso, viene utilizzato l'algoritmo corrente.

</dd> <dt>

<span id="MCI_QUALITY_DIALOG"></span><span id="mci_quality_dialog"></span>\_finestra di \_ dialogo qualità MCI
</dt> <dd>

Il driver di dispositivo dovrebbe visualizzare una finestra di dialogo per specificare il livello di qualità. Nella finestra di dialogo sono presenti campi specifici dell'algoritmo usati internamente dal driver di dispositivo per creare una struttura che descrive un livello di qualità specifico.

</dd> <dt>

<span id="MCI_QUALITY_HANDLE"></span><span id="mci_quality_handle"></span>\_handle di qualità MCI \_
</dt> <dd>

Il membro **dwHandle** della struttura identificata da *lpQuality* contiene un handle per una struttura. La struttura contiene dati specifici dell'algoritmo che descrivono il livello di qualità specifico. Il formato delle strutture per gli algoritmi è dipendente dal dispositivo.

</dd> <dt>

<span id="MCI_QUALITY_ITEM"></span><span id="mci_quality_item"></span>\_elemento qualità \_ MCI
</dt> <dd>

Una costante che indica il tipo di algoritmo è inclusa nel membro **dwItem** della struttura identificata da *lpQuality*.

</dd> <dt>

<span id="MCI_QUALITY_NAME"></span><span id="mci_quality_name"></span>\_nome qualità \_ MCI
</dt> <dd>

Il membro **lpstrName** della struttura identificata da *lpQuality* contiene un indirizzo di un buffer contenente il descrittore di qualità.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Mmsystem. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Comandi MCI](mci-commands.md)
</dt> </dl>

 

