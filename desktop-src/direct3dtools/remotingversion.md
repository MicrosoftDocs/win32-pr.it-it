---
description: Enumerazione utilizzata per indicare quale versione del protocul di comunicazione remota viene utilizzata.
MS-HAID: vspixengine.REMOTINGVERSION
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Enumerazione REMOTINGVERSION
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 598E9586-05FF-4889-BBAF-44814EEF203A
api_name:
- REMOTINGVERSION
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: a813453f9b5d1a89525e5b67cc22659281d04cb5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341591"
---
# <a name="span-idvspixengineremotingversionspanremotingversion-enumeration"></a><span id="vspixengine.remotingversion"></span>Enumerazione REMOTINGVERSION

Enumerazione utilizzata per indicare quale versione del protocul di comunicazione remota viene utilizzata.

## <a name="syntax"></a>Sintassi


```C++
};
```

## <a name="constants"></a>Costanti

<span id="REMOTING_DEV12"></span><span id="remoting_dev12"></span>**\_DEV12 remoto**  
Valore che indica che è in uso il protocollo di comunicazione remota di Visual Studio 2013 RTM.

<span id="REMOTING_DEV12_UPDATE_1"></span><span id="remoting_dev12_update_1"></span>**\_Aggiornamento DEV12 \_ remoto \_ 1**  
Valore che indica che è in uso il protocollo di comunicazione remota Visual Studio 2013 Update 1.

<span id="REMOTING_DEV12_UPDATE_4"></span><span id="remoting_dev12_update_4"></span>**\_ \_ Aggiornamento 4 di DEV12 Remoting \_**  
Valore che indica che è in uso il protocollo di comunicazione remota Visual Studio 2013 Update 4.

<span id="REMOTING_DEV14"></span><span id="remoting_dev14"></span>**\_DEV14 remoto**  
Valore che indica che è in uso il protocollo di comunicazione remota di Visual Studio 2015 RTM.

<span id="REMOTING_WIN10"></span><span id="remoting_win10"></span>**\_WIN10 remoto**  
Valore che indica che è in uso il protocollo di comunicazione remota di Windows 10 (a partire da Windows 10, la diagnostica della grafica è un componente del sistema operativo)

<span id="REMOTING_WIN10_JAN_2015"></span><span id="remoting_win10_jan_2015"></span>**Comunicazione remota \_ WIN10 \_ Jan \_ 2015**  
Valore che indica che viene utilizzato il protocollo di comunicazione remota di Windows 10 (gennaio 2015).

<span id="REMOTING_WIN10_JAN_2015_1"></span><span id="remoting_win10_jan_2015_1"></span>**Comunicazione remota \_ WIN10 \_ Jan \_ 2015 \_ 1**  
Valore che indica che viene utilizzato il protocollo di comunicazione remota di Windows 10 (gennaio 2015, V1).

<span id="REMOTING_WIN10_JAN_2015_2"></span><span id="remoting_win10_jan_2015_2"></span>**Comunicazione remota \_ WIN10 \_ Jan \_ 2015 \_ 2**  
Valore che indica che viene utilizzato il protocollo di comunicazione remota di Windows 10 (gennaio 2015, v2). Questa versione del protocollo ha introdotto richieste per la visualizzazione di risorse affiancate.

<span id="REMOTING_WIN10_JAN_2015_3"></span><span id="remoting_win10_jan_2015_3"></span>**Comunicazione remota \_ WIN10 \_ Jan \_ 2015 \_ 3**  
Valore che indica che viene utilizzato il protocollo di comunicazione remota di Windows 10 (gennaio 2015, V3). Questa versione del protocollo ha introdotto IPixEngine7, ora deprecata, per verificare il supporto della versione dell'interfaccia.

<span id="REMOTING_IPIXENGINE7_VERSION_CHECKING"></span><span id="remoting_ipixengine7_version_checking"></span>**\_Controllo della \_ versione di IPIXENGINE7 Remoting \_**  
Valore che indica che viene utilizzato il protocollo di comunicazione remota di Windows 10 (gennaio 2015, V1). Questa versione del protocollo si allontana dal basarsi su REMOTINGVERSION per mediare le funzionalità del protocollo. Il GUID dell'interfaccia è ora modificato quando int non pubblico

<span id="REMOTING_WIN10_FEB_2015_1"></span><span id="remoting_win10_feb_2015_1"></span>**Comunicazione remota \_ WIN10 \_ feb \_ 2015 \_ 1**  
Valore che indica che viene utilizzato il protocollo di comunicazione remota di Windows 10 (gennaio 2015, V1). Questa versione del protocollo introduce le proprietà delle informazioni di riepilogo con ID fissi univoci.

<span id="REMOTING_WIN10_2015_03_00"></span><span id="remoting_win10_2015_03_00"></span>**Comunicazione remota \_ WIN10 \_ 2015 \_ 03 \_ 00**  
Valore che indica che viene utilizzato il protocollo di comunicazione remota di Windows 10 (gennaio 2015, V1). Questa versione del protocollo ha introdotto il supporto per la finestra di stato di DirectX11.

<span id="REMOTING_LATES"></span><span id="remoting_lates"></span>**Servizi REMOti in \_ ritardo**  
Valore che indica che è in uso il protocollo .NET Remoting più recente.

## <a name="requirements"></a>Requisiti

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



