---
title: Struttura ORPC_DBG_ALL
description: La \_ struttura ORPC dbg \_ All viene utilizzata per passare parametri ai metodi dell'interfaccia IOrpcDebugNotify.
ms.assetid: 05371beb-9202-40a6-96d2-4b91497e2ee9
keywords:
- COM struttura ORPC_DBG_ALL
- Puntatore a struttura LPORPC_DBG_ALL COM
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
ms.openlocfilehash: a17f5b09e5fe2f668bf2bcd21e2e7fe6f0f766a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119366"
---
# <a name="orpc_dbg_all-structure"></a>\_Struttura ORPC dbg \_ All

La struttura **ORPC \_ dbg \_ All** viene utilizzata per passare parametri ai metodi dell'interfaccia [**IOrpcDebugNotify**](iorpcdebugnotify.md) .

> [!Note]  
> Ogni metodo dell'interfaccia [**IOrpcDebugNotify**](iorpcdebugnotify.md) utilizza una combinazione diversa dei membri seguenti. Se un membro non è indicato come usato da un metodo, non è definito quando viene passato al metodo.

 

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

Puntatore a un buffer di **byte** che contiene:

-   Primi quattro byte: caratteri ASCII "MARB" in ordine di memoria crescente.
-   Successivi 16 byte: **GUID** che identifica la notifica chiamata. Contiene uno dei seguenti elementi:
    1.  [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md): 9ED14F80-9673-101A-B07B-00DD01113F11
    2.  [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md):D a45f3e0-9673-101A-B07B-00DD01113F11
    3.  [**ClientNotify**](iorpcdebugnotify-clientnotify.md): 4F60E540-9674-101A-B07B-00DD01113F11
    4.  [**ServerNotify**](iorpcdebugnotify-servernotify.md): 1084FA00-9674-101A-B07B-00DD01113F11
    5.  [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md): 22080240-9674-101A-B07B-00DD01113F11
    6.  [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md): 2FC09500-9674-101A-B07B-00DD01113F11
-   Successivi quattro byte: riservati per un uso futuro.

> [!Note]
>
> Utilizzato da tutti i metodi dell'interfaccia [**IOrpcDebugNotify**](iorpcdebugnotify.md) .

 

</dd> <dt>

**pMessage**
</dt> <dd>

Puntatore a una struttura [**RPCOLEMESSAGE**](/windows/win32/api/objidlbase/ns-objidlbase-rpcolemessage) che contiene informazioni di marshalling dei dati RPC.

> [!Note]
>
> Utilizzato dai metodi [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)e [**ServerNotify**](iorpcdebugnotify-servernotify.md) .

 

</dd> <dt>

**REFIID**
</dt> <dd>

Puntatore all'IID dell'interfaccia [**IOrpcDebugNotify**](iorpcdebugnotify.md) .

> [!Note]
>
> Utilizzato dai metodi [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)e [**ServerNotify**](iorpcdebugnotify-servernotify.md) .

 

</dd> <dt>

**pChannel**
</dt> <dd>

Puntatore all'interfaccia [**Metodo IRpcChannelBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer) dell'implementazione del canale RPC com sul server.

> [!Note]
>
> Utilizzato dai metodi [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)e [**ServerNotify**](iorpcdebugnotify-servernotify.md) .

 

</dd> <dt>

**pUnkProxyMgr**
</dt> <dd>

Puntatore all'interfaccia [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) dell'oggetto che ha richiesto la chiamata al debugger. Può essere **null**, tuttavia, riduce la funzionalità del debugger.

> [!Note]
>
> Utilizzato dai metodi [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md)e [**ClientNotify**](iorpcdebugnotify-clientnotify.md) .

 

</dd> <dt>

**pInterface**
</dt> <dd>

Puntatore all'interfaccia COM del metodo che verrà richiamato da questa RPC. Non può essere **null**.

> [!Note]
>
> Utilizzato dai metodi [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)e [**ServerNotify**](iorpcdebugnotify-servernotify.md) .

 

</dd> <dt>

**pUnkObject**
</dt> <dd>

Deve essere **null**.

> [!Note]
>
> Utilizzato dai metodi [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)e [**ServerNotify**](iorpcdebugnotify-servernotify.md) .

 

</dd> <dt>

**HRESULT**
</dt> <dd>

Le modifiche a scopo di questo membro per ognuna delle notifiche seguenti:

[**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md): numero di byte che il debugger client trasmetterà al debugger del server. Se è zero, non è necessario trasmettere alcuna informazione.

[**ClientNotify**](iorpcdebugnotify-clientnotify.md): **HRESULT** dell'ultima RPC.

[**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md): numero di byte che il debugger client trasmetterà al debugger del server. Se è zero, non è necessario trasmettere alcuna informazione.

> [!Note]
>
> Utilizzato dai metodi [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md)e [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md) .

 

</dd> <dt>

**pvBuffer**
</dt> <dd>

Puntatore a una struttura [**di \_ \_ buffer di ORPC dbg**](orpc-dbg-buffer.md) che contiene le informazioni di debug con marshalling RPC. Non è definito se **cbBuffer** è zero.

> [!Note]
>
> Utilizzato dai metodi [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md)e [**ServerNotify**](iorpcdebugnotify-servernotify.md) .

 

</dd> <dt>

**cbBuffer**
</dt> <dd>

Lunghezza, in byte, dei dati a cui punta **pvBuffer**.

> [!Note]
>
> Utilizzato dai metodi [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md)e [**ServerNotify**](iorpcdebugnotify-servernotify.md) .

 

</dd> <dt>

**lpcbBuffer**
</dt> <dd>

Numero di byte che il debugger client trasmetterà al debugger del server. Se è zero, non è necessario trasmettere alcuna informazione. Questo valore sostituisce il valore restituito in **HRESULT**.

> [!Note]
>
> Utilizzato dai metodi [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md) .

 

</dd> <dt>

**riservati**
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

[**\_buffer dbg \_ ORPC**](orpc-dbg-buffer.md)
</dt> <dt>

[**\_argomenti init \_ ORPC**](orpc-init-args.md)
</dt> <dt>

[**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md)
</dt> <dt>

[**IOrpcDebugNotify**](iorpcdebugnotify.md)
</dt> </dl>

 

