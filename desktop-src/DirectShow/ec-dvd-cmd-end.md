---
description: Segnala che è stato completato un particolare comando del navigatore DVD.
ms.assetid: f460db8e-b966-41fa-bfa1-4ad3fa65c3e3
title: EC_DVD_CMD_END (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CMD_END
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 550a3969ba431127b05234a0c9fe38eb5938ebf2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325044"
---
# <a name="ec_dvd_cmd_end"></a>\_ \_ fine cmd DVD \_ EC

Segnala che è stato completato un particolare comando del [navigatore DVD](dvd-navigator-filter.md) .

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Identificatore del comando. Passare questo parametro al metodo [**IDvdInfo2:: GetCmdFromEvent**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcmdfromevent) per recuperare un puntatore a interfaccia [**IDvdCmd**](/windows/desktop/api/Strmif/nn-strmif-idvdcmd) .

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Valore **HRESULT** che indica lo stato del comando.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questo evento viene generato solo se l'applicazione imposta il flag SendEvents del DVD del \_ \_ flag CMD \_ in un metodo [**IDVDControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) che accetta un flag di [**\_ \_ flag CMD di DVD**](/windows/win32/api/strmif/ne-strmif-dvd_cmd_flags) .

Questo evento viene generato nel dominio del titolo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dvdevcode. h (include dshow. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Applicazioni DVD](dvd-applications.md)
</dt> <dt>

[Codici di notifica degli eventi DVD](dvd-notification-codes.md)
</dt> <dt>

[Notifica degli eventi in DirectShow](event-notification-in-directshow.md)
</dt> <dt>

[Sincronizzazione dei comandi DVD](synchronizing-dvd-commands.md)
</dt> </dl>

 

 




