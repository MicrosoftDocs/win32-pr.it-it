---
description: Contiene i risultati dell'esecuzione di una query sul database di shim per un eseguibile corrispondente.
ms.assetid: 6e6df118-fb64-4a97-9280-050e3b4e3a4b
title: Struttura SDBQUERYRESULT
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SDBQUERYRESULT
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9c631438d36116d47bfcb8675c390fb2974271c8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966034"
---
# <a name="sdbqueryresult-structure"></a>Struttura SDBQUERYRESULT

Contiene i risultati dell'esecuzione di una query sul database di shim per un eseguibile corrispondente.

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagSDBQUERYRESULT {
  TAGREF atrExes[SDB_MAX_EXES];
  DWORD  adwExeFlags[SDB_MAX_EXES];
  TAGREF atrLayers[SDB_MAX_LAYERS];
  DWORD  dwLayerFlags;
  TAGREF trApphelp;
  DWORD  dwExeCount;
  DWORD  dwLayerCount;
  GUID   guidID;
  DWORD  dwFlags;
  DWORD  dwCustomSDBMap;
  GUID   rgGuidDB[SDB_MAX_SDBS];
} SDBQUERYRESULT, *PSDBQUERYRESULT;
```



## <a name="members"></a>Members

<dl> <dt>

**atrExes**
</dt> <dd>

Valori **TAGREF** dei file eseguibili corrispondenti. Si noti che **sdb \_ Max \_ exe** viene definito come 16.

</dd> <dt>

**adwExeFlags**
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

**atrLayers**
</dt> <dd>

Valori **TAGREF** dei livelli corrispondenti. Si noti che i **\_ \_ livelli SDB max** sono definiti come 8.

</dd> <dt>

**dwLayerFlags**
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

**trApphelp**
</dt> <dd>

Valore **TAGREF** del messaggio AppHelp del file eseguibile corrispondente.

</dd> <dt>

**dwExeCount**
</dt> <dd>

Numero di elementi in **atrExes**.

</dd> <dt>

**dwLayerCount**
</dt> <dd>

Numero di elementi in **atrLayers**.

</dd> <dt>

**guidID**
</dt> <dd>

GUID dell'ultimo file eseguibile.

</dd> <dt>

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

**dwCustomSDBMap**
</dt> <dd>

Mappa dei database di shim personalizzati. I bit corrispondenti vengono impostati se **rgGuidDB** è valido.

</dd> <dt>

**rgGuidDB**
</dt> <dd>

GUID dei database shim. Si noti che **sdb \_ Max \_ SDB** è definito come 16.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SdbGetMatchingExe**](sdbgetmatchingexe.md)
</dt> </dl>

 

 




