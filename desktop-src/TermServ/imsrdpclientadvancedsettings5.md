---
title: Interfaccia IMsRdpClientAdvancedSettings5
description: Gestisce le impostazioni client avanzate. Deriva dall'interfaccia IMsRdpClientAdvancedSettings4.
ms.assetid: a927cd4c-7f70-493e-a4f6-056d0352d56e
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto , descritta
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49ad2b26697cd3985cc0e39a8ed7345bc4bbe941
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622347"
---
# <a name="imsrdpclientadvancedsettings5-interface"></a>Interfaccia IMsRdpClientAdvancedSettings5

Gestisce le impostazioni client avanzate. Deriva [**dall'interfaccia IMsRdpClientAdvancedSettings4.**](imsrdpclientadvancedsettings4.md)

Per ottenere un'istanza di questa interfaccia, usare la proprietà [**IMsTscAx::AdvancedSettings**](imstscax-advancedsettings.md) per ottenere un puntatore a interfaccia [**IMsTscAdvancedSettings.**](imstscadvancedsettings-interface.md) Chiamare quindi [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sul **puntatore IMsTscAdvancedSettings** e passare **\_ IID IMsRdpClientAdvancedSettings5** **a QueryInterface**.

## <a name="members"></a>Membri

**L'interfaccia IMsRdpClientAdvancedSettings5** eredita da [**IMsRdpClientAdvancedSettings4.**](imsrdpclientadvancedsettings4.md) **IMsRdpClientAdvancedSettings5** include anche questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

**L'interfaccia IMsRdpClientAdvancedSettings5** ha queste proprietà.



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th >Proprietà</th>
<th >Tipo di accesso</th>
<th >Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td ><a href="imsrdpclientadvancedsettings5-audioredirectionmode.md"><strong>AudioRedirectionMode</strong></a><br/></td>
<td >Lettura/Scrittura<br/></td>
<td >Modalità di reindirizzamento audio. La <a href="imsrdpclientadvancedsettings5-audioredirectionmode.md"><strong>proprietà AudioRedirectionMode</strong></a> ha i valori possibili seguenti.<br/>
<dt><span id="AUDIO_MODE_REDIRECT___0"></span><span id="audio_mode_redirect___0"></span><strong>AUDIO_MODE_REDIRECT 0</strong> (il reindirizzamento audio è abilitato e l'opzione per il reindirizzamento è &quot; Bring to this computer &quot; . Questa è la modalità predefinita.<br/> </dt> <dd></dd> <dt><span id="AUDIO_MODE_PLAY_ON_SERVER_1"></span><span id="audio_mode_play_on_server_1"></span><strong>AUDIO_MODE_PLAY_ON_SERVER 1</strong> (il reindirizzamento audio è abilitato e l'opzione &quot; è Lascia nel computer remoto &quot; . L'opzione Lascia nel computer remoto è supportata solo quando ci si connette in remoto a un computer host che esegue &quot; &quot; Windows Vista. Se la connessione è a un computer host che esegue Windows Server 2008, l'opzione Lascia nel computer remoto viene modificata in Non &quot; &quot; &quot; &quot; riprodurre.<br/> </dt> <dd></dd> <dt><span id="AUDIO_MODE_NONE_2"></span><span id="audio_mode_none_2"></span><strong>AUDIO_MODE_NONE 2</strong> (il reindirizzamento audio è abilitato e la modalità è &quot; Non &quot; riprodurre).<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td ><a href="imsrdpclientadvancedsettings5-bitmapvirtualcache32bppsize.md"><strong>BitmapVirtualCache32BppSize</strong></a><br/></td>
<td >Lettura/Scrittura<br/></td>
<td >Specifica le dimensioni del file della cache virtuale per bitmap bpp (32 bit per pixel). Il valore massimo è 48 megabyte (MB).<br/></td>
</tr>
<tr class="odd">
<td ><a href="imsrdpclientadvancedsettings5-connectionbarshowpinbutton.md"><strong>ConnectionBarShowPinButton</strong></a><br/></td>
<td >Lettura/Scrittura<br/></td>
<td >Specifica se il pulsante aggiungi deve essere visualizzato sulla barra delle connessioni. Per impostazione predefinita, il valore è <strong>TRUE.</strong><br/></td>
</tr>
<tr class="even">
<td ><a href="imsrdpclientadvancedsettings5-publicmode.md"><strong>PublicMode</strong></a><br/></td>
<td >Lettura/Scrittura<br/></td>
<td >Specifica se la modalità pubblica deve essere abilitata o disabilitata. Per impostazione predefinita, la modalità pubblica è impostata su <strong>FALSE.</strong><br/></td>
</tr>
<tr class="odd">
<td ><a href="imsrdpclientadvancedsettings5-redirectclipboard.md"><strong>RedirectClipboard</strong></a><br/></td>
<td >Lettura/Scrittura<br/></td>
<td >Specifica se il reindirizzamento degli Appunti deve essere abilitato o disabilitato. Per impostazione predefinita, la modalità di reindirizzamento degli Appunti è <strong>impostata su TRUE</strong> (abilitata).<br/></td>
</tr>
<tr class="even">
<td ><a href="imsrdpclientadvancedsettings5-redirectdevices.md"><strong>RedirectDevices</strong></a><br/></td>
<td >Lettura/Scrittura<br/></td>
<td >Specifica se i dispositivi reindirizzati devono essere abilitati o disabilitati. Per impostazione predefinita, la modalità dei dispositivi reindirizzati è impostata su <strong>FALSE.</strong><br/></td>
</tr>
<tr class="odd">
<td ><a href="imsrdpclientadvancedsettings5-redirectposdevices.md"><strong>RedirectPOSDevices</strong></a><br/></td>
<td >Lettura/Scrittura<br/></td>
<td >Specifica se i dispositivi reindirizzati al punto di servizio devono essere abilitati o disabilitati. Per impostazione predefinita, la modalità dei dispositivi reindirizzati al punto di servizio è impostata su <strong>FALSE.</strong><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Commenti

Questa interfaccia è stata estesa dalle interfacce seguenti, con ogni nuova interfaccia che eredita tutti i metodi e le proprietà delle interfacce precedenti:

-   [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
-   [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
-   [**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                         |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                   |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings5 è definito come FBA7F64E-6783-4405-DA45-FA4A763DABD0<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md)
</dt> <dt>

[Connessione Web Desktop remoto informazioni di riferimento](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

