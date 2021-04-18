---
title: Metodi di proprietà IADsSyntax (IADs. h)
description: I metodi di proprietà dell'interfaccia IADsSyntax ottengono o impostano le proprietà elencate nella tabella seguente. Per ulteriori informazioni sui metodi di proprietà, vedere Metodi della proprietà di interfaccia.
ms.assetid: a216a55d-63eb-4fdf-a67f-8d4b5eb74262
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsSyntax ADSI
topic_type:
- apiref
api_name:
- IADsSyntax Property Methods
- IADsSyntax.OleAutoDataType
- IADsSyntax.get_OleAutoDataType
- IADsSyntax.put_OleAutoDataType
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7a41c84efb4f48171913156823e18a301236290
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517656"
---
# <a name="iadssyntax-property-methods"></a>Metodi di proprietà IADsSyntax

I metodi di proprietà dell'interfaccia [**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax) ottengono o impostano le proprietà elencate nella tabella seguente. Per ulteriori informazioni sui metodi di proprietà, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).

## <a name="properties"></a>Proprietà

<dl> <dt>

**OleAutoDataType**
</dt> <dd> <dl>

Recupera e imposta un oggetto **Long** che contiene il valore della costante **VT \_ xxx** per il tipo di dati di automazione che rappresenta questa sintassi.

Active Directory supporta le seguenti costanti **VT \_ xxx** per il tipo di dati di automazione che rappresenta questa sintassi:

-   **VT \_ bool bool**
-   **VT \_** BSTR BSTR
-   **VT \_ bstrt bstrt**
-   **VT \_ valuta CY**
-   **VT \_ Data data**
-   **VT \_** **null** vuoto
-   **VT \_ ERRORE** non valido
-   **VT \_ I2** Short
-   **VT \_ I4** Long
-   **VT \_ R4** Real
-   **VT \_ Doppio R8**
-   **VT \_ BYTE UI1**

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OleAutoDataType(
  [out] LONG* plAutoDataType
);
HRESULT put_OleAutoDataType(
  [in] LONG lAutoDataType
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>Commenti

Una matrice di byte senza segno, la **\_** \| **\_ matrice VT** Ui1 VT potrebbe significare che il provider ha eseguito il mapping di una sintassi di cui non è possibile eseguire il mapping a un tipo virtuale di automazione.

## <a name="examples"></a>Esempio

Nell'esempio di codice seguente viene esaminata la sintassi dell'attributo **OperatingSystemVersion** di un computer in una rete tramite il provider WinNT. La sintassi del risultato è una stringa.


```VB
Dim obj As IADs
Dim cl As IADsClass
Dim pr As IADsProperty
Dim sy As IADsSyntax
Dim sc As IADsContainer
On Error GoTo Cleanup

Set obj = GetObject("WinNT://myMachine,computer")
Set cl = GetObject(obj.Schema)
Set sc = GetObject(cl.Parent)
Set pr = sc.GetObject("Property","OperatingSystemVersion")
Set sy = GetObject(sc.ADsPath & "/" & pr.Syntax)
 
MsgBox "Automation data types: " & sy.OleAutoDataType

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set obj = Nothing
    Set cl = Nothing
    Set pr = Nothing
    Set sy = Nothing
    Set sc = Nothing
```



Nell'esempio di codice seguente viene esaminata la sintassi dell'attributo **OperatingSystemVersion** di un computer in una rete tramite il provider WinNT. La sintassi del risultato è una stringa. Per brevità, il controllo degli errori viene omesso.


```C++
#include <stdio.h>
#include <activeds.h>
#include <atlbase.h>
 
IADs *pObj = NULL;
IADsClass *pCls = NULL;
IADsProperty *pProp = NULL;
IADsSyntax *pSyn = NULL;
IADsContainer *pCont = NULL;
 
HRESULT hr = ADsGetObject(L"WinNT://myMachine,computer",
                          IID_IADs,
                          (void**)&pObj);
if(FAILED(hr)){goto Cleanup;}
VARIANT var;
VariantInit(&var);
CComBSTR sbstr;
 
pObj->get_Schema(&sbstr);
printf("Object schema: %S\n",sbstr);
 
hr = ADsGetObject(sbstr, IID_IADsClass,(void**)&pCls);
if(FAILED(hr)){goto Cleanup;}

pCls->get_Parent(&sbstr);
printf("Object class's container:  %S\n", sbstr);
 
hr = ADsGetObject(sbstr, IID_IADsContainer, (void**)&pCont);
if(FAILED(hr)){goto Cleanup;}
pCont->QueryInterface(IID_IADs,(void**)&pObj);
pObj->get_ADsPath(&sbstr);
printf("Container's AdsPath:  %S\n",sbstr);
 
IDispatch *pDisp;
hr = pCont->GetObject(CComBSTR("Property"),
                      CComBSTR("OperatingSystemVersion"),
                      (IDispatch**)&pDisp);
if(FAILED(hr)){goto Cleanup;}
 
hr = pDisp->QueryInterface(IID_IADsProperty, (void**)&pProp);
if(FAILED(hr)){goto Cleanup;}
 
hr = pProp->get_Syntax(&sbstr);
if(FAILED(hr)){goto Cleanup;}
printf("Property Syntax:  %S\n",sbstr);
 
printf("ADsPath of the syntax object %S\n",sbstr);
 
hr = ADsGetObject(sbstr, IID_IADsSyntax, (void**)&pSyn);
if(FAILED(hr)){goto Cleanup;}

long lType;
pSyn->get_OleAutoDataType(&lType);
printf("Property syntax's OleAutoDataType: %d\n", lType);

Cleanup:
    if(pObj)
        pObj->Release();

    if(pProp)
        pProp->Release();

    if(pCls)
        pCls->Release();

    if(pSyn)
        pSyn->Release();

    if(pCont)
        pCont->Release();
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>IADs. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsSyntax è definito come C8F93DD2-4AE0-11CF-9E73-00AA004A5691<br/>           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass)
</dt> <dt>

[**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)
</dt> <dt>

[**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax)
</dt> </dl>

 

 





