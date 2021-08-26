---
description: Segnala che è stato avviato un comando DVD Navigator.
ms.assetid: 230116b4-23f1-4c37-a781-da2c5aa20a1f
title: EC_DVD_CMD_START (Dvdevcode.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CMD_START
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 418163b55699f8ba7c38026764f3326985d7e1788369729f42067cff62a56949
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998081"
---
# <a name="ec_dvd_cmd_start"></a>EC \_ DVD \_ CMD \_ START

Segnala che è stato avviato un comando [DVD Navigator.](dvd-navigator-filter.md)

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Identificatore del comando. Passare questo parametro al metodo [**IDvdInfo2::GetCmdFromEvent**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcmdfromevent) per recuperare un puntatore a interfaccia [**IDvdCmd.**](/windows/desktop/api/Strmif/nn-strmif-idvdcmd)

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

**Valore HRESULT** che indica lo stato del comando.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questo evento viene generato solo se l'applicazione imposta il flag **\_ \_ \_ SendEvents DVD CMD FLAG** in un metodo [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) che accetta un flag [**DVD CMD \_ \_ FLAGS.**](/windows/win32/api/strmif/ne-strmif-dvd_cmd_flags)

Questo evento viene generato nel dominio del titolo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dvdevcode.h (includere Dshow.h)</dt> </dl> |



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

 

 




