---
title: Interfaccia IMsTscAdvancedSettings
description: Include metodi per recuperare e impostare le proprietà che abilitano la memorizzazione nella cache, la compressione e il reindirizzamento degli Appunti e della stampante bitmap.
ms.assetid: 3385e843-be05-4801-8d59-6395d95686b1
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsTscAdvancedSettings Servizi Desktop remoto
- Interfaccia IMsTscAdvancedSettings Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad4d55df30c940ecc5a5515f13c05a285507499e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301626"
---
# <a name="imstscadvancedsettings-interface"></a>Interfaccia IMsTscAdvancedSettings

Include metodi per recuperare e impostare le proprietà che abilitano la memorizzazione nella cache, la compressione e il reindirizzamento degli Appunti e della stampante bitmap. È anche possibile specificare i nomi delle dll client del canale virtuale.

Per ottenere un'istanza di questa interfaccia, è possibile usare la proprietà [**IMsTscAx:: AdvancedSettings**](imstscax-advancedsettings.md) .

## <a name="members"></a>Membri

L'interfaccia **IMsTscAdvancedSettings** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IMsTscAdvancedSettings** dispone anche di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'interfaccia **IMsTscAdvancedSettings** ha queste proprietà.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Proprietà</th>
<th style="text-align: left;">Tipo di accesso</th>
<th style="text-align: left;">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="imstscadvancedsettings-allowbackgroundinput.md"><strong>allowBackgroundInput</strong></a><br/></td>
<td style="text-align: left;">Lettura/Scrittura<br/></td>
<td style="text-align: left;">Specifica se la modalità di input in background è abilitata.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscadvancedsettings-bitmapperistence.md"><strong>BitmapPeristence</strong></a><br/></td>
<td style="text-align: left;">Lettura/Scrittura<br/></td>
<td style="text-align: left;">Specifica se la memorizzazione nella cache bitmap è abilitata.<br/>
<blockquote>
[!Note]<br />
L'errore di ortografia nel nome della proprietà si trova nella versione rilasciata del controllo.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscadvancedsettings-compress.md"><strong>Comprimere</strong></a><br/></td>
<td style="text-align: left;">Lettura/Scrittura<br/></td>
<td style="text-align: left;">Specifica se la compressione è abilitata.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscadvancedsettings-containerhandledfullscreen.md"><strong>ContainerHandledFullScreen</strong></a><br/></td>
<td style="text-align: left;">Lettura/Scrittura<br/></td>
<td style="text-align: left;">Specifica se la modalità a schermo intero gestita dal contenitore è abilitata.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscadvancedsettings-disablerdpdr.md"><strong>DisableRdpdr</strong></a><br/></td>
<td style="text-align: left;">Lettura/Scrittura<br/></td>
<td style="text-align: left;">Specifica se il reindirizzamento della stampante e degli Appunti è abilitato.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscadvancedsettings-iconfile.md"><strong>IconFile</strong></a><br/></td>
<td style="text-align: left;">Sola scrittura<br/></td>
<td style="text-align: left;">Specifica il nome del file che contiene i dati dell'icona a cui sarà possibile accedere quando viene visualizzato il client in modalità schermo intero.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscadvancedsettings-iconindex.md"><strong>IconIndex</strong></a><br/></td>
<td style="text-align: left;">Sola scrittura<br/></td>
<td style="text-align: left;">Specifica l'indice dell'icona all'interno del file icona corrente.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscadvancedsettings-keyboardlayoutstr.md"><strong>KeyBoardLayoutStr</strong></a><br/></td>
<td style="text-align: left;">Sola scrittura<br/></td>
<td style="text-align: left;">Specifica il nome dell'identificatore delle impostazioni locali di input attivo (denominato in precedenza il layout della tastiera) da usare per la connessione.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscadvancedsettings-plugindlls.md"><strong>PluginDlls</strong></a><br/></td>
<td style="text-align: left;">Sola scrittura<br/></td>
<td style="text-align: left;">Specifica i nomi delle dll client del canale virtuale da caricare.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Commenti

Questa interfaccia è stata estesa dalle interfacce seguenti, in cui ogni nuova interfaccia eredita tutti i metodi e le proprietà delle interfacce precedenti:

-   [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
-   [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
-   [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md)
-   [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
-   [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
-   [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
-   [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)

Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                  |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                            |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| IID<br/>                      | IID \_ IMsTscAdvancedSettings è definito come 809945cc-4b3b-4A92-a6b0-dbf9b5f2ef2d<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[Riferimento Connessione Web Desktop remoto](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

