---
description: Contiene informazioni sui dati di AppHelp.
ms.assetid: 31b305e9-1f38-4952-b4fd-963df79b1346
title: Struttura APPHELP_DATA
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- APPHELP_DATA
api_type:
- NA
api_location: ''
ms.openlocfilehash: 20c66779dcb3d89746de5f90b2817ddcdb37b59f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304458"
---
# <a name="apphelp_data-structure"></a>\_Struttura dei dati APPHELP

Contiene informazioni sui dati di AppHelp.

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagAPPHELP_DATA {
  DWORD  dwFlags;
  DWORD  dwSeverity;
  DWORD  dwHTMLHelpID;
  LPTSTR szAppName;
  TAGREF trExe;
  LPTSTR szURL;
  LPTSTR szLink;
  LPTSTR szAppTitle;
  LPTSTR szContact;
  LPTSTR szDetails;
  DWORD  dwData;
  BOOL   bSPEntry;
} APPHELP_DATA, *PAPPHELP_DATA;
```



## <a name="members"></a>Members

<dl> <dt>

**dwFlags**
</dt> <dd>

Il parametro può essere costituito da uno o più dei valori seguenti.

<dl> <dt>

<span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**SHIMREG \_ Disabilita \_ shim** (0x00000001)
</dt> <dt>

<span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**SHIMREG \_ DISABILITARE \_ APPHELP** (0x00000002)
</dt> <dt>

<span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**SHIMREG \_ APPHELP \_ NOUI** (0x00000004)
</dt> <dt>

<span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**SHIMREG \_ \_Annullamento APPHELP** (0x10000000)
</dt> <dt>

<span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**SHIMREG \_ Disabilita \_ SxS** (0x00000010)
</dt> <dt>

<span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**SHIMREG \_ DISABLE \_ Layer** (0x00000020)
</dt> <dt>

<span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**SHIMREG \_ Disabilita \_ driver** (0x00000040)
</dt> </dl> </dd> <dt>

**dwSeverity**
</dt> <dd>

Questo parametro può essere APPTYPE \_ None (0).

</dd> <dt>

**dwHTMLHelpID**
</dt> <dd>

Identificatore della Guida HTML.

</dd> <dt>

**szAppName**
</dt> <dd>

Nome dell'applicazione.

</dd> <dt>

**trExe**
</dt> <dd>

[**TAGREF**](tagref.md) del file eseguibile corrispondente.

</dd> <dt>

**szURL**
</dt> <dd>

URL per il collegamento di AppHelp online.

</dd> <dt>

**szLink**
</dt> <dd>

Testo del collegamento per **szURL**.

</dd> <dt>

**szAppTitle**
</dt> <dd>

Titolo del messaggio AppHelp.

</dd> <dt>

**szContact**
</dt> <dd>

Informazioni di contatto del fornitore.

</dd> <dt>

**szDetails**
</dt> <dd>

Messaggio AppHelp dettagliato.

</dd> <dt>

**dwData**
</dt> <dd>

Dati definiti dall'utente gestiti dall'applicazione.

</dd> <dt>

**bSPEntry**
</dt> <dd>

Questo membro è **true** se questa voce si trova nel database di Service Pack e **false** in caso contrario.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SdbReadApphelpDetailsData**](sdbreadapphelpdetailsdata.md)
</dt> </dl>

 

 




