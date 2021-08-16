---
title: ORPC_DBG_ALL struttura
description: La struttura ORPC DBG ALL viene usata per passare parametri \_ \_ ai metodi dell'interfaccia IOrpcDebugNotify.
ms.assetid: 05371beb-9202-40a6-96d2-4b91497e2ee9
keywords:
- ORPC_DBG_ALL struttura COM
- LPORPC_DBG_ALL puntatore alla struttura COM
topic_type:
- apiref
api_name:
- ORPC_DBG_ALL
api_location:
- N/A
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 359e3b3ec2530917c6a502da90ea86771238319687f8dcf8e9b7862e4ddf1954
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118310305"
---
# <a name="orpc_dbg_all-structure"></a>Struttura ORPC \_ DBG \_ ALL

La **struttura ORPC \_ DBG \_ ALL** viene usata per passare parametri ai metodi dell'interfaccia [**IOrpcDebugNotify.**](iorpcdebugnotify.md)

> [!Note]  
> Ogni metodo [**dell'interfaccia IOrpcDebugNotify**](iorpcdebugnotify.md) usa una combinazione diversa dei membri seguenti. Se un membro non viene indicato come usato da un metodo, non è definito quando viene passato a tale metodo.

 

## <a name="syntax"></a>Sintassi


```C++
typedef struct ORPC_DBG_ALL {
  BYTE              *pSignature;
  RPCOLEMESSAGE     *pMessage;
  const IID         *refiid;
  IRpcChannelBuffer *pChannel;
  IUnknown          *pUnkProxyMgr;
  void              *pInterface;
  IUnknown          *pUnkObject;
  HRESULT           hresult;
  void              *pvBuffer;
  ULONG             *cbBuffer;
  ULONG             *lpcbBuffer;
  void              *reserved;
} ORPC_DBG_ALL, *LPORPC_DBG_ALL;
```



## <a name="members"></a>Members

<dl> <dt>

**pSignature**
</dt> <dd>

Puntatore a un buffer **BYTE** che contiene:

-   Primi quattro byte: i caratteri ASCII "MARB" in ordine di memoria crescente.
-   16 byte successivi: **GUID che** identifica la notifica chiamata. Contiene uno degli elementi seguenti:
    1.  [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md): 9ED14F80-9673-101A-B07B-00DD01113F11
    2.  [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md):D A45F3E0-9673-101A-B07B-00DD01113F11
    3.  [**ClientNotify**](iorpcdebugnotify-clientnotify.md):4F60E540-9674-101A-B07B-00DD01113F11
    4.  [**ServerNotify**](iorpcdebugnotify-servernotify.md):1084FA00-9674-101A-B07B-00DD01113F11
    5.  [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md):22080240-9674-101A-B07B-00DD01113F11
    6.  [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md):2FC09500-9674-101A-B07B-00DD01113F11
-   Quattro byte successivi: riservati per un uso futuro.

> [!Note]
>
> Usato da tutti i metodi [**dell'interfaccia IOrpcDebugNotify.**](iorpcdebugnotify.md)

 

</dd> <dt>

**pMessage**
</dt> <dd>

Puntatore a una [**struttura RPCOLEMESSAGE**](/windows/win32/api/objidlbase/ns-objidlbase-rpcolemessage) che contiene informazioni di marshalling dei dati RPC.

> [!Note]
>
> Usato dai [**metodi ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)e [**ServerNotify.**](iorpcdebugnotify-servernotify.md)

 

</dd> <dt>

**refiid**
</dt> <dd>

Puntatore all'IID [**dell'interfaccia IOrpcDebugNotify.**](iorpcdebugnotify.md)

> [!Note]
>
> Usato dai [**metodi ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)e [**ServerNotify.**](iorpcdebugnotify-servernotify.md)

 

</dd> <dt>

**pChannel**
</dt> <dd>

Puntatore [**all'interfaccia IRpcChannelBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer) dell'implementazione del canale RPC COM nel server.

> [!Note]
>
> Usato dai [**metodi ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)e [**ServerNotify.**](iorpcdebugnotify-servernotify.md)

 

</dd> <dt>

**pUnkProxyMgr**
</dt> <dd>

Puntatore [**all'interfaccia IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) dell'oggetto interessato da questa chiamata del debugger. Può essere **NULL,** tuttavia, riduce le funzionalità del debugger.

> [!Note]
>
> Usato dai [**metodi ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md)e [**ClientNotify.**](iorpcdebugnotify-clientnotify.md)

 

</dd> <dt>

**pInterface**
</dt> <dd>

Puntatore all'interfaccia COM del metodo che verrà richiamato da questo RPC. Non deve essere **NULL.**

> [!Note]
>
> Usato dai [**metodi ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)e [**ServerNotify.**](iorpcdebugnotify-servernotify.md)

 

</dd> <dt>

**pUnkObject**
</dt> <dd>

Deve essere **NULL.**

> [!Note]
>
> Usato dai [**metodi ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)e [**ServerNotify.**](iorpcdebugnotify-servernotify.md)

 

</dd> <dt>

**Hresult**
</dt> <dd>

Lo scopo di questo membro cambia per ognuna delle notifiche seguenti:

[**ClientGetBufferSize:**](iorpcdebugnotify-clientgetbuffersize.md)numero di byte che il debugger client trasmetterà al debugger server. Se zero, non è necessario trasmettere alcuna informazione.

[**ClientNotify:**](iorpcdebugnotify-clientnotify.md) **HRESULT dell'ultima** RPC.

[**ServerGetBufferSize:**](iorpcdebugnotify-servergetbuffersize.md)numero di byte che il debugger client trasmetterà al debugger server. Se zero, non è necessario trasmettere alcuna informazione.

> [!Note]
>
> Usato dai [**metodi ClientGetBufferSize,**](iorpcdebugnotify-clientgetbuffersize.md) [**ClientNotify**](iorpcdebugnotify-clientnotify.md)e [**ServerGetBufferSize.**](iorpcdebugnotify-servergetbuffersize.md)

 

</dd> <dt>

**pvBuffer**
</dt> <dd>

Puntatore a una [**struttura BUFFER \_ DBG \_ ORPC**](orpc-dbg-buffer.md) che contiene le informazioni di debug con marshalling RPC. Non è definito se **cbBuffer** è zero.

> [!Note]
>
> Usato dai [**metodi ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md)e [**ServerNotify.**](iorpcdebugnotify-servernotify.md)

 

</dd> <dt>

**cbBuffer**
</dt> <dd>

Lunghezza, in byte, dei dati a cui punta **pvBuffer**.

> [!Note]
>
> Usato dai [**metodi ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md)e [**ServerNotify.**](iorpcdebugnotify-servernotify.md)

 

</dd> <dt>

**lpcbBuffer**
</dt> <dd>

Numero di byte che il debugger client trasmetterà al debugger server. Se zero, non è necessario trasmettere alcuna informazione. Questo valore sostituisce il valore restituito in **hresult**.

> [!Note]
>
> Usato dai [**metodi ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize.**](iorpcdebugnotify-clientgetbuffersize.md)

 

</dd> <dt>

**Riservati**
</dt> <dd>

Riservato. Non usare.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                     |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>N/D</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ORPC \_ DBG \_ BUFFER**](orpc-dbg-buffer.md)
</dt> <dt>

[**ORPC \_ INIT \_ ARGS**](orpc-init-args.md)
</dt> <dt>

[**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md)
</dt> <dt>

[**IOrpcDebugNotify**](iorpcdebugnotify.md)
</dt> </dl>

 

