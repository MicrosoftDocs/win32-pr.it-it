---
description: La struttura EXPERTENUMINFO fornisce informazioni sull'esperto.
ms.assetid: f745997b-d753-4c4d-88b6-6978f5eaa91c
title: Struttura EXPERTENUMINFO (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTENUMINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 46942f1140cbb5f74685b16e468b68b85221deceeae2509a9d0676261898e238
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939038"
---
# <a name="expertenuminfo-structure"></a>Struttura EXPERTENUMINFO

La **struttura EXPERTENUMINFO** fornisce informazioni sull'esperto. Network Monitor alloca memoria per la struttura e la passa all'esperto quando chiama la [**funzione Register Expert.**](register-expert.md) Quando l'esperto riceve la struttura, deve quindi inserire tutte le informazioni che Network Monitor richieste.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  char                szName[EXPERTSTRINGLENGTH];
  char                szVendor[EXPERTSTRINGLENGTH];
  char                szDescription[EXPERTSTRINGLENGTH];
  DWORD               Version;
  DWORD               Flags;
  HEXPERT             hExpert;
  char                szDllName[MAX_PATH];
  HINSTANCE           hModule;
  PEXPERTREGISTERPROC pRegisterProc;
  PEXPERTCONFIGPROC   pConfigProc;
  PEXPERTRUNPROC      pRunProc;
} EXPERTENUMINFO, *PEXPERTENUMINFO;
```



## <a name="members"></a>Members

<dl> <dt>

**Szname**
</dt> <dd>

Nome dell'esperto.

</dd> <dt>

**szVendor**
</dt> <dd>

Nome del fornitore che crea l'esperto.

</dd> <dt>

**szDescription**
</dt> <dd>

Descrizione dell'esperto. Il valore del **membro szDescription** può essere **NULL.** Se il nome è troppo lungo, viene troncato nella configurazione predefinita del visualizzatore.

</dd> <dt>

**Version**
</dt> <dd>

Il valore deve essere zero.

</dd> <dt>

**Flag**
</dt> <dd>

I flag seguenti descrivono l'esperto.



| Valore                                                                                                                                                                                                                                                    | Significato                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span id="EXPERT_ENUM_FLAG_CONFIGURABLE"></span><span id="expert_enum_flag_configurable"></span><dl> <dt>**EXPERT \_ ENUM \_ FLAG \_ CONFIGURABLE**</dt> </dl>                                          | L'esperto supporta le chiamate al [**metodo Configure.**](configure.md) <br/>        |
| <span id="EXPERT_ENUM_FLAG_VIEWER_PRIVATE"></span><span id="expert_enum_flag_viewer_private"></span><dl> <dt>**EXPERT \_ ENUM \_ FLAG \_ VIEWER \_ PRIVATE**</dt> </dl>                                   | L'esperto richiede un'istanza privata (non Visualizzatore eventi. <br/>                       |
| <span id="EXPERT_ENUM_FLAG_NO_VIEWER"></span><span id="expert_enum_flag_no_viewer"></span><dl> <dt>**EXPERT \_ ENUM \_ FLAG \_ NO \_ VIEWER**</dt> </dl>                                                  | L'esperto non invia notifiche degli eventi. <br/>                                  |
| <span id="EXPERT_ENUM_FLAG_ADD_ME_TO_RMC_IN_SUMMARY"></span><span id="expert_enum_flag_add_me_to_rmc_in_summary"></span><dl> <dt>**EXPERT \_ ENUM \_ FLAG \_ ADD \_ ME \_ TO \_ RMC \_ IN \_ SUMMARY**</dt> </dl> | Quando lo stato attivo si trova nel riquadro di riepilogo, l'esperto viene visualizzato nel menu di scelta rapida. <br/> |
| <span id="EXPERT_ENUM_FLAG_ADD_ME_TO_RMC_IN_DETAIL"></span><span id="expert_enum_flag_add_me_to_rmc_in_detail"></span><dl> <dt>**EXPERT ENUM FLAG ADD ME TO RMC IN DETAIL (AGGIUNTA DEL FLAG EXPERT \_ ENUM \_ A \_ \_ \_ \_ RMC \_ IN \_ DETTAGLIO)**</dt> </dl>    | Quando lo stato attivo si trova nel riquadro dei dettagli, l'esperto viene visualizzato nel menu di scelta rapida. <br/>  |



 

</dd> <dt>

**hExpert**
</dt> <dd>

Gestire per l'esperto. Quando la **struttura EXPERTENUMINFO** viene usata per registrare un esperto, il parametro viene ignorato.

</dd> <dt>

**szDllName**
</dt> <dd>

Membro privato; non utilizzare .

</dd> <dt>

**Hmodule**
</dt> <dd>

Membro privato; non utilizzare .

</dd> <dt>

**pRegisterProc**
</dt> <dd>

Membro privato; non utilizzare .

</dd> <dt>

**pConfigProc**
</dt> <dd>

Membro privato; non utilizzare .

</dd> <dt>

**pRunProc**
</dt> <dd>

Membro privato; non utilizzare .

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




