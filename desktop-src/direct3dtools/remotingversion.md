---
description: Enumerazione utilizzata per indicare la versione del protoculo remoto in uso.
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
ms.openlocfilehash: d7e5c937610b06a58309181a4dad2c95846d287b335c8ab6b2fed9008f338f3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985481"
---
# <a name="span-idvspixengineremotingversionspanremotingversion-enumeration"></a><span id="vspixengine.remotingversion"></span>Enumerazione REMOTINGVERSION

Enumerazione utilizzata per indicare la versione del protoculo remoto in uso.

## <a name="syntax"></a>Sintassi


```C++
};
```

## <a name="constants"></a>Costanti

<span id="REMOTING_DEV12"></span><span id="remoting_dev12"></span>**COMUNICAZIONE \_ REMOTA DEV12**  
Valore che indica che è in Visual Studio 2013 protocollo di comunicazione remota RTM.

<span id="REMOTING_DEV12_UPDATE_1"></span><span id="remoting_dev12_update_1"></span>**REMOTING \_ DEV12 \_ UPDATE \_ 1**  
Valore che indica che viene usato il Visual Studio 2013 remoto dell'aggiornamento 1.

<span id="REMOTING_DEV12_UPDATE_4"></span><span id="remoting_dev12_update_4"></span>**REMOTING \_ DEV12 \_ UPDATE \_ 4**  
Valore che indica che il Visual Studio 2013 Update 4 remoto è in uso.

<span id="REMOTING_DEV14"></span><span id="remoting_dev14"></span>**COMUNICAZIONE \_ REMOTA DEV14**  
Valore che indica che viene usato il Visual Studio remoto RTM 2015.

<span id="REMOTING_WIN10"></span><span id="remoting_win10"></span>**COMUNICAZIONE \_ REMOTA WIN10**  
Valore che indica che è in Windows 10 protocollo di comunicazione remota (a partire da Windows 10, la diagnostica della grafica è un componente del sistema operativo)

<span id="REMOTING_WIN10_JAN_2015"></span><span id="remoting_win10_jan_2015"></span>**COMUNICAZIONE \_ REMOTA WIN10 \_ GENNAIO \_ 2015**  
Valore che indica che è in Windows 10 protocollo di comunicazione remota di Windows 10 (gennaio 2015).

<span id="REMOTING_WIN10_JAN_2015_1"></span><span id="remoting_win10_jan_2015_1"></span>**COMUNICAZIONE \_ REMOTA WIN10 \_ GENNAIO \_ 2015 \_ 1**  
Valore che indica che viene Windows 10 protocollo di comunicazione remota Windows 10 (gennaio 2015, v1).

<span id="REMOTING_WIN10_JAN_2015_2"></span><span id="remoting_win10_jan_2015_2"></span>**COMUNICAZIONE \_ REMOTA WIN10 \_ GENNAIO \_ 2015 \_ 2**  
Valore che indica che viene Windows 10 protocollo di comunicazione remota di Windows 10 (gennaio 2015, v2). Questa versione del protocollo ha introdotto richieste per la visualizzazione di risorse affiancate.

<span id="REMOTING_WIN10_JAN_2015_3"></span><span id="remoting_win10_jan_2015_3"></span>**COMUNICAZIONE \_ REMOTA WIN10 \_ GENNAIO \_ 2015 \_ 3**  
Valore che indica che viene Windows 10 protocollo di comunicazione remota di Windows 10 (gennaio 2015, v3). Questa versione del protocollo ha introdotto IPixEngine7, ora deprecato, per il controllo del supporto della versione dell'interfaccia.

<span id="REMOTING_IPIXENGINE7_VERSION_CHECKING"></span><span id="remoting_ipixengine7_version_checking"></span>**CONTROLLO \_ DELLA VERSIONE DI IPIXENGINE7 PER LA COMUNICAZIONE \_ \_ REMOTA**  
Valore che indica che viene Windows 10 protocollo di comunicazione remota Windows 10 (gennaio 2015, v1). Questa versione del protocollo non si basa su REMOTINGVERSION per mediare le funzionalità del protocollo. Il GUID dell'interfaccia viene ora modificato quando int non pubblico

<span id="REMOTING_WIN10_FEB_2015_1"></span><span id="remoting_win10_feb_2015_1"></span>**COMUNICAZIONE \_ REMOTA WIN10 \_ FEB \_ 2015 \_ 1**  
Valore che indica che viene Windows 10 protocollo di comunicazione remota Windows 10 (gennaio 2015, v1). Questa versione del protocollo introduce proprietà di informazioni di riepilogo con ID fissi univoci.

<span id="REMOTING_WIN10_2015_03_00"></span><span id="remoting_win10_2015_03_00"></span>**COMUNICAZIONE \_ REMOTA WIN10 \_ 2015 \_ 03 \_ 00**  
Valore che indica che viene Windows 10 protocollo di comunicazione remota Windows 10 (gennaio 2015, v1). Questa versione del protocollo ha introdotto il supporto per la finestra di stato di DirectX11.

<span id="REMOTING_LATES"></span><span id="remoting_lates"></span>**LATES \_ DI COMUNICAZIONE REMOTA**  
Valore che indica che viene usato il protocollo di comunicazione remota più recente.

## <a name="requirements"></a>Requisiti

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



