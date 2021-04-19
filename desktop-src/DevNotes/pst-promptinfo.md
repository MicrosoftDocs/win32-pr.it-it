---
description: Definisce il comportamento di richiesta dell'archivio protetto ogni volta che viene visualizzata un'interfaccia utente.
ms.assetid: 413bcb33-5fe9-4ba1-b65f-3e53a7cbf70c
title: Struttura PST_PROMPTINFO (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_PROMPTINFO
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: da499ea3d6f5037e9f1e745771112840a462f11d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328036"
---
# <a name="pst_promptinfo-structure"></a>\_Struttura PROMPTINFO PST

\[L'archiviazione protetta (PStore) è disponibile per l'uso in Windows Server 2003 e Windows XP. È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive. PStore usa un'implementazione precedente della protezione dei dati. Gli sviluppatori sono vivamente invitati a sfruttare i vantaggi della protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Definisce il comportamento di richiesta dell'archivio protetto ogni volta che viene visualizzata un'interfaccia utente.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  DWORD      cbSize;
  DWORD      dwPromptFlags;
  DWORD_PTR  hwndApp;
  LPCWSTR    szPrompt;
} PST_PROMPTINFO, *PPST_PROMPTINFO;
```



## <a name="members"></a>Members

<dl> <dt>

**cbSize**
</dt> <dd>

Dimensione della struttura.

</dd> <dt>

**dwPromptFlags**
</dt> <dd>

Questo flag viene ignorato.



| Valore                                                                                                                                                                                                                                          | Significato                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span id="PST_PF_ALWAYS_SHOW"></span><span id="pst_pf_always_show"></span><dl> <dt>**Pst \_ PF \_ \_ Mostra sempre**</dt> <dt>0x00000001</dt> </dl> | Richiede che il provider visualizzi la finestra di dialogo di richiesta all'utente anche se non è necessaria per l'accesso. <br/> |
| <span id="PST_PF_NEVER_SHOW"></span><span id="pst_pf_never_show"></span><dl> <dt>**Pst \_ PF \_ non \_ Mostra mai**</dt> <dt>0x00000002</dt> </dl>    | Non visualizzare la finestra di dialogo di richiesta all'utente.<br/>                                                                 |



 

</dd> <dt>

**hwndApp**
</dt> <dd>

Handle per la finestra padre dell'interfaccia utente. Il membro **hwndApp** determina la posizione in cui viene visualizzata l'interfaccia utente. Se viene passato **null** , il desktop viene considerato la finestra padre.

</dd> <dt>

**szPrompt**
</dt> <dd>

Stringa di richiesta.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PStore. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DeleteItem**](ipstore-deleteitem.md)
</dt> <dt>

[**OpenItem**](ipstore-openitem.md)
</dt> <dt>

[**ReadItem**](ipstore-readitem.md)
</dt> <dt>

[**WriteItem**](ipstore-writeitem.md)
</dt> </dl>

 

 
