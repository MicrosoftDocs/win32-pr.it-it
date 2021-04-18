---
description: Il decodificatore Windows Media Audio decodifica i flussi audio codificati dal codificatore Windows Media Audio.
ms.assetid: 2d8e4a97-34a7-4eee-9567-7ae98fa282b9
title: Decodificatore Windows Media Audio (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70f11242f237b8d9709baea6d445a8426236913c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325954"
---
# <a name="windows-media-audio-decoder"></a>Decodificatore Windows Media Audio

Il decodificatore Windows Media Audio decodifica i flussi audio codificati dal [**codificatore Windows Media Audio**](windowsmediaaudioencoder.md). Il codificatore e il decodificatore supportano tre categorie di audio codificato: Windows Media Audio standard, Windows Media Audio Professional e Windows Media Audio Lossless.

## <a name="class-identifier"></a>Identificatore di classe

L'identificatore di classe (CLSID) per il decodificatore Windows Media Audio è rappresentato dalla costante **CLSID \_ CWMADecMediaObject**. È possibile creare un'istanza del decodificatore audio chiamando **CoCreateInstance**.

## <a name="input-formats"></a>Formati di input

La tabella seguente illustra i tag di formato audio che rappresentano le categorie di input supportate dal decodificatore Windows Media Audio. Per informazioni su come impostare i tipi di input e output per il decodificatore, vedere [configurazione della decodifica audio](configuringaudiodecoding.md).



| Costante tag di formato             | Valore del tag di formato | Formato audio                     |
|---------------------------------|------------------|----------------------------------|
| \_Formato Wave \_ WMAUDIO2          | 0x0161           | Windows Media Audio standard     |
| \_Formato Wave \_ WMAUDIO3          | 0x0162           | Windows Media Audio Professional |
| \_formato Wave \_ WMAUDIO \_ Lossless | 0x0163           | Windows Media Audio senza perdita di perdite     |



 

## <a name="output-formats"></a>Formati di output

La tabella seguente illustra i tag di formato audio che rappresentano i tipi di output supportati dal **Decodificatore Windows Media Audio**. Per informazioni su come impostare i tipi di input e output per il decodificatore, vedere [Configuring audio encoding](configuringaudioencoding.md).



| Costante tag di formato       | Valore del tag di formato | Formato audio                                          |
|---------------------------|------------------|-------------------------------------------------------|
| \_PCM in formato Wave \_         | 0x0001           | Formato PCM                                            |
| \_formato Wave \_ IEEE \_ float | 0x0003           | Virgola mobile IEEE                                   |
| \_formato Wave \_ estendibile  | 0xFFFE           | Formato PCM/IEEE nella struttura **WAVEFORMATEXTENSIBLE** |



 

## <a name="interfaces"></a>Interfacce

Un oggetto Decoder audio espone l'interfaccia **IMediaObject** in modo che l'oggetto possa essere usato come DMO (DirectX Media Object) ed espone l'interfaccia **IMFTransform** in modo che l'oggetto possa essere usato come trasformazione Media Foundation (MFT).

Un decodificatore Windows Media Audio si comporta come DMO o MFT, a seconda delle interfacce ottenute e della versione di Windows in esecuzione. Nella tabella seguente vengono illustrate le condizioni in base alle quali un decodificatore audio si comporta come DMO o MFT.



| Sistema operativo | Comportamento del decodificatore                                                                                                                                                                      |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP       | Un decodificatore Windows Media Audio si comporta sempre come DMO.                                                                                                                                |
| Windows Vista    | Per impostazione predefinita, un decodificatore Windows Media Audio si comporta come DMO. Se si ottiene un'interfaccia **IMFTransform** o un'interfaccia **IPropertyStore** su un decodificatore audio, si comporta come un MFT. |
| Windows 7        | Per impostazione predefinita, un decodificatore Windows Media Audio si comporta come DMO. Se si ottiene un'interfaccia **IMFTransform** su un decodificatore audio, si comporta come un MFT.                                    |



 

## <a name="properties"></a>Proprietà

Il decodificatore Windows Media Audio supporta le seguenti proprietà.



<table>
<thead>
<tr class="header">
<th>Proprietà</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mfpkey-decoder-maxnumpcmsampleswithpaddedsilenceproperty.md"><strong>MFPKEY_Decoder_MaxNumPCMSamplesWithPaddedSilence</strong></a></td>
<td>Specifica il numero massimo di campioni PCM aggiuntivi che potrebbero essere restituiti alla fine della decodifica di un file.<br/> <dl> Windows Vista e versioni successive.<br />
Standard, Professional, lossless.<br />
Di sola lettura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmadec-drcmodeproperty.md"><strong>MFPKEY_WMADEC_DRCMODE</strong></a></td>
<td>Specifica la modalità di controllo dell'intervallo dinamico che viene utilizzata dal decodificatore audio.<br/> <dl> Windows XP e versioni successive.<br />
Standard, Professional, lossless.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmadec-folddown-matrixproperty.md"><strong>MFPKEY_WMADEC_FOLDDOWN_MATRIX</strong></a></td>
<td>Specifica i coefficienti di riduzione forniti dall'autore per la decodifica dell'audio multicanale per un numero di canali inferiore rispetto al contenuto del flusso codificato. <br/> <dl> Windows XP e versioni successive.<br />
Professionale<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmadec-hiresoutputproperty.md"><strong>MFPKEY_WMADEC_HIRESOUTPUT</strong></a></td>
<td>Specifica se il decodificatore audio deve fornire un output a risoluzione elevata.<br/> <dl> Windows XP e versioni successive.<br />
Professionale, senza perdita di perdite.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmadec-ltrtoutputproperty.md"><strong>MFPKEY_WMADEC_LTRTOUTPUT</strong></a></td>
<td>Specifica se il decodificatore audio deve eseguire Lt-Rt riduzioni.<br/> <dl> Windows Vista e versioni successive.<br />
Professional.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmadec-spkrcfgproperty.md"><strong>MFPKEY_WMADEC_SPKRCFG</strong></a></td>
<td>Specifica la configurazione dell'altoparlante nel computer client.<br/> <dl> Windows XP e versioni successive.<br />
Professional.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmadrc-avgrefproperty.md"><strong>MFPKEY_WMADRC_AVGREF</strong></a></td>
<td>Specifica il livello di volume medio del contenuto audio.<br/> <dl> Windows XP e versioni successive.<br />
Professionale, senza perdita di perdite.<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmadrc-avgtargetproperty.md"><strong>MFPKEY_WMADRC_AVGTARGET</strong></a></td>
<td>Specifica il livello di volume medio desiderato per il contenuto audio di output.<br/> <dl> Windows XP e versioni successive.<br />
Professionale, senza perdita di perdite.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmadrc-peakrefproperty.md"><strong>MFPKEY_WMADRC_PEAKREF</strong></a></td>
<td>Specifica il livello di volume massimo che si verifica nel contenuto audio.<br/> <dl> Windows XP e versioni successive.<br />
Professionale, senza perdita di perdite.<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmadrc-peaktargetproperty.md"><strong>MFPKEY_WMADRC_PEAKTARGET</strong></a></td>
<td>Specifica il livello di volume massimo desiderato per il contenuto audio di output.<br/> <dl> Windows XP e versioni successive.<br />
Professionale, senza perdita di perdite.<br />
Sola scrittura.<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows XP, Windows Vista o Windows 7<br/>                                       |
| Intestazione<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmadmod.dll</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti codec](codecobjects.md)
</dt> <dt>

[Implementazione del codec](codecimplementation.md)
</dt> </dl>

 

 




