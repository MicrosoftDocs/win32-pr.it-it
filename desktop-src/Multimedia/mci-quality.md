---
title: MCI_QUALITY comando (Mmsystem.h)
description: Il comando MCI QUALITY definisce un livello di qualità personalizzato per la compressione dei dati \_ audio, video o immagine. I dispositivi video digitali riconoscono questo comando.
ms.assetid: 91ad9704-0089-4b1f-b0f6-919ab5fd84e0
keywords:
- MCI_QUALITY comando Windows Multimedia
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
ms.openlocfilehash: 1237d9b70c9f06782342c404c19dd23cf6f0848f8c7b33523bce35990287fa27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138222"
---
# <a name="mci_quality-command"></a>Comando MCI \_ QUALITY

Il comando MCI QUALITY definisce un livello di qualità personalizzato per la compressione dei dati \_ audio, video o immagine. I dispositivi video digitali riconoscono questo comando.

Per inviare questo comando, chiamare [**la funzione mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


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

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*Dwflags*
</dt> <dd>

MCI \_ NOTIFY, MCI \_ WAIT o MCI \_ TEST. Per informazioni su questi flag, vedere [Wait, Notify e Test Flags.](the-wait-notify-and-test-flags.md)

</dd> <dt>

<span id="lpQuality"></span><span id="lpquality"></span><span id="LPQUALITY"></span>*lpQuality*
</dt> <dd>

Puntatore a [**una struttura MCI \_ DGV \_ QUALITY \_ PARMS.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_quality_parmsa)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

Il nome definito per questo livello di qualità può essere usato durante l'impostazione dell'audio, del video o della qualità con i comandi [MCI \_ SETAUDIO](mci-setaudio.md) e [MCI \_ SETVIDEO.](mci-setvideo.md)

I flag aggiuntivi seguenti si applicano ai dispositivi video digitali:

<dl> <dt>

<span id="MCI_QUALITY_ALG"></span><span id="mci_quality_alg"></span>MCI \_ QUALITY \_ ALG
</dt> <dd>

Il **membro lpstrAlgorithm** della struttura identificata da *lpQuality* contiene un indirizzo di un buffer contenente il nome dell'algoritmo. Questo algoritmo deve essere supportato dal driver di dispositivo e deve essere compatibile con il descrittore audio, still o video usato. Se questo flag viene omesso, viene utilizzato l'algoritmo corrente.

</dd> <dt>

<span id="MCI_QUALITY_DIALOG"></span><span id="mci_quality_dialog"></span>FINESTRA DI DIALOGO QUALITÀ MCI \_ \_
</dt> <dd>

Il driver di dispositivo dovrebbe visualizzare una finestra di dialogo per specificare il livello di qualità. La finestra di dialogo contiene campi specifici dell'algoritmo usati internamente dal driver di dispositivo per creare una struttura che descrive un livello di qualità specifico.

</dd> <dt>

<span id="MCI_QUALITY_HANDLE"></span><span id="mci_quality_handle"></span>HANDLE DI QUALITÀ MCI \_ \_
</dt> <dd>

Il **membro dwHandle** della struttura identificata da *lpQuality* contiene un handle per una struttura . La struttura contiene dati specifici dell'algoritmo che descrivono il livello di qualità specifico. Il formato delle strutture per gli algoritmi dipende dal dispositivo.

</dd> <dt>

<span id="MCI_QUALITY_ITEM"></span><span id="mci_quality_item"></span>ELEMENTO DI QUALITÀ MCI \_ \_
</dt> <dd>

Una costante che indica il tipo di algoritmo è inclusa nel **membro dwItem** della struttura identificata da *lpQuality*.

</dd> <dt>

<span id="MCI_QUALITY_NAME"></span><span id="mci_quality_name"></span>NOME \_ QUALITÀ MCI \_
</dt> <dd>

Il **membro lpstrName** della struttura identificata da *lpQuality* contiene l'indirizzo di un buffer contenente il descrittore di qualità.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Mmsystem.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[Comandi MCI](mci-commands.md)
</dt> </dl>

 

